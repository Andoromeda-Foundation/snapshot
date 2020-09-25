<template>
  <header class="header">
    <div class="h-logo">
      <router-link :to="{ name: 'home' }">
        <img src="@/assets/image/logo.svg" alt="logo" class="hl-logo" />
      </router-link>
      <h2 class="hl-title">项目列表</h2>
    </div>
    <div class="h-btn">
      <button class="hb-connect">链接钱包</button>
      <!-- <div class="hb-language">
        0
      </div> -->
    </div>
  </header>
</template>

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
