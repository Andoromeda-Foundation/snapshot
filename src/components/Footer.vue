<template>
  <footer class="footer">
    <img
      src="@/assets/image/footer-logo.png"
      alt="footer"
      class="footer-logo"
    />
    <section class="f-nav">
      <a class="fn-item" href="#" v-for="item in 8" :key="item">
        <img src="" alt="" />
      </a>
    </section>
  </footer>
</template>

<style lang="scss" scoped>
.footer {
  width: 100%;
  height: 214px;
  background-color: #000;
}
.footer-logo {
  height: 138px;
  margin-top: 16px;
}
</style>
