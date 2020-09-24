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
        <a href="javascript:;" class="t-active">交易</a>
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
            <p class="ti-des">
              波场上的DAO+SNXSNXSNXSNXSXSNXSNXSXSNXSNXSXSNXSNXSNXSNX+KNC
            </p>
            <section class="ti-btn">
              <a href="javascript:;">现货交易</a>
              <a href="javascript:;">理财</a>
            </section>
          </section>
          <section class="ti-logo">
            <img
              src="https://static.debank.com/project-logo/yam.finance_logo_400x400-1597213129331.png"
              alt="logo"
            />
          </section>
        </section>
      </section>
    </section>

    <Footer></Footer>
  </div>
</template>

<style lang="scss" scoped>
.home {
  background-color: #eceff6;
}
.banner {
  height: 350px;
  text-align: center;
  .banner-img {
    max-width: 1920px;
    width: 100%;
    height: 100%;
    margin: 0 auto;
    object-fit: cover;
  }
}

.container {
  max-width: 740px;
  padding: 0 10px;
  margin: 0 auto;
  box-sizing: border-box;
}

.tab-head {
  margin-top: 24px;
  .th-title {
    font-size: 16px;
    font-weight: 500;
    color: #333333;
    line-height: 22px;
    padding: 0;
    margin: 8px 0;
  }
}
.th-line {
  width: 100%;
  height: 4px;
  background: #dde1eb;
  .thl-active {
    width: 120px;
    height: 4px;
    background: #2eafb4;
  }
}

.toggle {
  margin: 24px 0;
  display: flex;
  a {
    width: 16.6666%;
    height: 40px;
    background: #ffffff;
    font-size: 14px;
    font-weight: 500;
    color: #333333;
    display: flex;
    align-items: center;
    justify-content: center;

    &.t-active {
      background-color: #2eafb4;
      color: #fff;
    }
  }
}

.toggle-container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-column-gap: 24px;
  grid-row-gap: 24px;
  margin-bottom: 60px;
}
.tc-item {
  background: #ffffff;
  border-radius: 4px;
  display: flex;
  justify-content: space-between;
  padding: 24px;
  box-sizing: border-box;
  overflow: hidden;
}

.ti-title {
  font-size: 24px;
  font-weight: 500;
  color: #333333;
  line-height: 33px;
  padding: 0;
  margin: 0;
}
.ti-des {
  font-size: 14px;
  font-weight: 400;
  color: #b2b2b2;
  line-height: 20px;
  padding: 0;
  margin: 0;
  word-break: break-all;
}
.ti-btn {
  margin-top: 38px;
  display: flex;
  a {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 72px;
    height: 24px;
    background: #e1f5f5;
    border-radius: 4px;

    font-size: 12px;
    font-weight: 500;
    color: #2eafb4;
    line-height: 17px;
    &:nth-child(1) {
      margin-right: 8px;
    }
  }
}
.ti-logo {
  width: 40px;
  height: 40px;
  flex: 0 0 40px;
  border-radius: 100%;
  overflow: hidden;
  margin-left: 20px;
  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
}
</style>
