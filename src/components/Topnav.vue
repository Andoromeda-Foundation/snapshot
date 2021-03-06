<template>
  <Sticky class="mb-4">
    <div
      v-if="config.env === 'develop'"
      class="p-3 text-center bg-blue"
      style="color: white; font-size: 20px;"
    >
      This is the demo site, give it a try!
    </div>
    <nav id="topnav" class="border-bottom width-full bg-black">
      <Container>
        <div class="d-flex flex-items-center" style="height: 78px;">
          <div class="flex-auto d-flex flex-items-center">
            <router-link
              :to="{ name: 'home' }"
              class="d-inline-block d-flex flex-items-center"
              style="font-size: 24px; padding-top: 4px;"
            >
              <span
                :class="space && 'hide-sm'"
                class="mr-1"
                v-text="'snapshot'"
              />
            </router-link>
            <router-link
              v-if="space"
              :to="{ name: 'proposals' }"
              class="d-inline-block d-flex flex-items-center"
              style="font-size: 24px; padding-top: 4px;"
            >
              <span class="pl-1 pr-2 text-gray" v-text="'/'" />
              <Token :space="space.key" symbolIndex="space" size="28" />
              <span class="ml-2" v-text="space.name" />
            </router-link>
          </div>
          <div :key="web3.account">
            <template v-if="$auth.isAuthenticated && !wrongNetwork">
              <UiButton
                @click="modalOpen = true"
                class="button-outline"
                :loading="loading"
              >
                <Avatar
                  :address="web3.account"
                  size="16"
                  class="mr-0 mr-sm-2 mr-md-2 mr-lg-2 mr-xl-2 ml-n1"
                />
                <span v-if="web3.name" v-text="web3.name" class="hide-sm" />
                <span v-else v-text="_shorten(web3.account)" class="hide-sm" />
              </UiButton>
            </template>
            <UiButton
              v-else-if="web3.injectedLoaded && wrongNetwork"
              class="text-red"
            >
              <Icon name="warning" class="ml-n1 mr-1 v-align-middle" />
              Wrong network
            </UiButton>
            <UiButton v-else @click="modalOpen = true" :loading="loading">
              Connect<span class="hide-sm" v-text="' wallet'" />
            </UiButton>
            <UiButton @click="modalAboutOpen = true" class="ml-2">
              <span v-text="'?'" class="ml-n1 mr-n1" />
            </UiButton>
          </div>
        </div>
        <ModalAccount
          :open="modalOpen"
          @close="modalOpen = false"
          @login="handleLogin"
        />
        <ModalAbout :open="modalAboutOpen" @close="modalAboutOpen = false" />
      </Container>
    </nav>
  </Sticky>
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
