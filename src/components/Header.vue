<template>
  <header class="header">
    <div class="h-logo">
      <router-link :to="{ name: 'home' }">
        <img src="@/assets/image/logo.svg" alt="logo" class="hl-logo" />
      </router-link>
      <h2 class="hl-title">项目列表</h2>
    </div>
    <div class="h-btn">
      <UiButton @click="modalOpen = true" :loading="loading">
        Connect<span class="hide-sm" v-text="' wallet'" />
      </UiButton>
      <button class="hb-connect" @click="modalOpen = true" :loading="loading">链接钱包</button>
      <!-- <div class="hb-language">
        0
      </div> -->
    </div>
    <ModalAccount
      :open="modalOpen"
      @close="modalOpen = false"
      @login="handleLogin"
    />
    <ModalAbout :open="modalAboutOpen" @close="modalAboutOpen = false" />
  </header>
</template>

<script>
import { mapActions } from 'vuex';

export default {
  data() {
    return {
      loading: false,
      modalOpen: false,
      modalAboutOpen: false
    };
  },
  computed: {
    wrongNetwork() {
      const chainId = process.env.VUE_APP_CHAIN_ID || 1;
      return parseInt(chainId) !== this.web3.network.chainId;
    },
    showLogin() {
      return (
        (!this.$auth.isAuthenticated && !this.web3.injectedLoaded) ||
        (!this.$auth.isAuthenticated && !this.wrongNetwork)
      );
    },
    space() {
      try {
        return this.web3.spaces[this.$route.params.key];
      } catch (e) {
        return {};
      }
    }
  },
  methods: {
    ...mapActions(['login']),
    async handleLogin(connector) {
      this.modalOpen = false;
      this.loading = true;
      await this.login(connector);
      this.loading = false;
    }
  }
};
</script>


<style lang="scss" scoped>
.header {
  height: 60px;
  background: #ffffff;
  box-shadow: 0px 2px 16px 0px rgba(0, 0, 0, 0.5);
  display: flex;
  padding: 0 24px;
  align-items: center;
  justify-content: space-between;
  box-sizing: border-box;
}
.h-logo {
  display: flex;
  align-items: center;
}
.hl-logo {
  height: 40px;
  color: #000;
}
.hl-title {
  font-size: 20px;
  font-weight: 500;
  color: #333333;
  line-height: 28px;
  padding: 0;
  margin: 0 0 0 60px;
}

.h-btn {
  display: flex;
  align-items: center;
}
.hb-connect {
  width: 160px;
  height: 40px;
  background: #2eafb4;
  border-radius: 4px;
  font-size: 16px;
  font-weight: 500;
  color: #ffffff;
  border: none;
  outline: none;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  &:hover {
    background: #269397;
  }
}
</style>
