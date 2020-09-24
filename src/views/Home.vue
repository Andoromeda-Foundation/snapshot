<template>
  <div class="home">
    <Header></Header>

    <section class="banner">
      <img
        src="@/assets/image/home-banner.png"
        alt="banner"
        class="banner-img"
      />
    </section>

    <section class="container">
      <section class="tab-head">
        <p class="th-title">以太坊网络</p>
        <section class="th-line">
          <section class="thl-active"></section>
        </section>
      </section>

      <section class="toggle">
        <a href="javascript:;">交易</a>
        <a href="javascript:;">交易</a>
        <a href="javascript:;">交易</a>
        <a href="javascript:;">交易</a>
        <a href="javascript:;">交易</a>
        <a href="javascript:;">交易</a>
      </section>

      <section class="toggle-container">
        <section class="tc-item" v-for="item in 6" :key="item">
          <section>
            <h4 class="ti-title">DACC 2.0</h4>
            <p class="ti-des">波场上的DAO+SNX+KNC</p>
            <section class="ti-btn">
              <a href="javascript:;">现货交易</a>
              <a href="javascript:;">理财</a>
            </section>
          </section>
          <img src="" alt="" />
        </section>
      </section>
    </section>

    <footer class="footer">
      <img src="" alt="">
      <section class="f-nav">
        <a class="fn-item" href="#" v-for="item in 8" :key="item">
          <img src="" alt="">
        </a>
      </section>
    </footer>
  </div>
</template>

<style lang="scss" scoped>
.banner {
  height: 350px;
  .banner-img {
    max-width: 1920px;
    width: 100%;
    height: 100%;
    margin: 0 auto;
    object-fit: cover;
  }
}
</style>
