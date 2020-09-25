<template>
  <footer class="footer">
    <section class="f-container">
      <div>
        <img
          src="@/assets/image/footer-logo.svg"
          alt="footer"
          class="footer-logo"
        />
        <p class="f-text">&copy;2020 4399DAO</p>
      </div>
      <section class="f-nav">
        <a class="fn-item" href="#" v-for="item in 8" :key="item">
          <img src="" alt="" />
        </a>
      </section>
    </section>
  </footer>
</template>

<style lang="scss" scoped>
.footer {
  width: 100%;

  box-sizing: border-box;
  height: 214px;
  background-color: #000;
}
.f-container {
  max-width: 1200px;
  padding: 0 20px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 100%;
}
.footer-logo {
  height: 50px;
  color: #fff;
}
.f-text {
  color: #fff;
  font-size: 18px;
  padding: 0;
  margin: 2px 0 0 0;
  line-height: 20px;
}

.f-nav {
  display: flex;
  align-items: center;
  height: 100%;
  .fn-item {
    width: 40px;
    height: 40px;
    border-radius: 100%;
    background-color: #595657;
    display: block;
    overflow: hidden;
    margin: 0 0 0 20px;
  }
}
</style>
