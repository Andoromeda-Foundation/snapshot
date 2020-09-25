<template>
  <section class="page">
    <Header></Header>
    <section class="banner">
      <section class="b-logo">
        <img src="https://static.debank.com/project-logo/yam.finance_logo_400x400-1597213129331.png" alt="logo">
      </section>
      <span class="b-title">BFT</span>
        <span class="b-description">流动性聚合协议</span>
        <section class="b-tag">
          <section class="bt-item">现货交易</section>
          <section class="bt-item">理财</section>
        </section>
    </section>
    <section class="container">
      <section class="c-head">
        <section class="ch-item">
          <h3 class="i-title">项目简介</h3>
          <p class="i-description">
            With the advent of popular decentralized exchanges, including UniSwap, the crypto industry saw the rise of permission-less trading platforms that could compete with centralized exchanges. In the year 2020, we’re living through a renascence of decentralization where entire ecosystems are bootstrapped to promote lending and alternative financial services built with blockchain technology.Early on, UniS…
          </p>
          <a href="" class="i-more">展开更多</a>
        </section>
        <section class="ch-item item-link">
          <h3 class="i-title">相关链接</h3>
          <p class="i-item">
            <span class="ii-name">官方网址</span>
            <a class="ii-link" href="https://berkshire.finance/#/">https://berkshire.finance/#/</a>
          </p>
          <p class="i-item">
            <span class="ii-name">官方网址</span>
            <a class="ii-link" href="https://berkshire.finance/#/">https://berkshire.finance/#/</a>
          </p>
          <p class="i-item">
            <span class="ii-name">官方网址</span>
            <section class="ii-share">
              <a href="">t</a>
              <a href="">t</a>
              <a href="">t</a>
              <a href="">t</a>
            </section>
          </p>
        </section>
        <section class="ch-item">
          <h3 class="i-title">挖矿信息</h3>
          <p class="i-item">
            <span class="ii-name">挖矿抵押币种</span>
            <section class="ii-content">
            ETH-XMX（uni-v2）       ETH-BFT（uni-v2）      $AAPL-ETH（uni-v2）
            USDT-ETH（uni-v2）     sUSD-ETH（uni-v2）    LEND-ETH （uni-v2）
            COMP-ETH（uni-v2）    YFII-ETH（uni-v2）       DAI-ETH（uni-v2）
            BET-ETH（uni-v2）        RenBTC-ETH（uni-v2）
            </section>
          </p>
          <p class="i-item">
            <span class="ii-name">挖矿抵押币种</span>
            <section class="ii-content">
              $AAPL-ETH挖矿地址<br>
              <a class="ii-link" href="https://berkshire.finance/#/actions/$AAPL-ETH/1">https://berkshire.finance/#/actions/$AAPL-ETH/1</a>
              <br>
              $AAPL-ETH挖矿地址<br>
              <a class="ii-link" href="https://berkshire.finance/#/actions/$AAPL-ETH/1">https://berkshire.finance/#/actions/$AAPL-ETH/1</a>
            </section>
          </p>
          <a class="i-more" href="">展开更多</a>

        </section>
        <section class="ch-item">
          <h3 class="i-title">项目信息</h3>
          <p class="i-item">
            <span class="ii-name">官方网址</span>
            <span class="ii-text">2500000枚</span>
          </p>
          <p class="i-item">
            <span class="ii-name">官方网址</span>
            <span class="ii-text">BFT-ETH矿池双倍奖励</span>
          </p>
          <p class="i-item">
            <span class="ii-name">官方网址</span>
            <a class="ii-link" href="https://berkshire.finance/#/">0x1ec1…47F03f1D36</a>
          </p>
          <p class="i-item">
            <span class="ii-name">官方网址</span>
            <span class="ii-text">知道创宇</span>
          </p>
        </section>
      </section>

      <section class="proposals">
        <p class="p-title">
          Proposals
          <span class="p-len">12</span>
        </p>
        <section class="p-content">
          <section class="pc-head">
            <a href="">All</a>
            <a href="">Core</a>
            <a href="">Community</a>
            <a href="">Active</a>
            <a href="">Pending</a>
            <a href="">Closed</a>
          </section>
          <ul class="pc-item">
            <li class="i-list" v-for="item in 5" :key="item">
              <span class="il-tag active">Active</span>
              <span class="il-title">Release free rewards</span>
              <section class="il-text">
                <span>#QmeaUEb</span> By 0x683A...De84
                <span class="ml-n1">
                  <span class="ilt-label">Core</span>
                </span>
                <span >50.84 YAM</span><!----> start <span>9/24/2020</span> end <span>9/27/2020</span>
              </section>
            </li>
          </ul>
        </section>
      </section>
    </section>
    <Footer></Footer>
  </section>
</template>

<style lang="scss" scoped>
.page {
  background-color: #eceff6;
  height: 100%;
}
.banner {
  height: 324px;
  background: #2eafb4;
  overflow: hidden;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.b-logo {
  width: 128px;
  height: 128px;
  border-radius: 100%;
  margin: 48px auto 0;
  overflow: hidden;
  img {
    widows: 100%;
    height: 100%;
    object-fit: cover;
  }
}
.b-title {
  font-size: 36px;
  font-weight: 500;
  color: #ffffff;
  line-height: 1;
  padding: 0;
  margin: 10px 0 0;
}
.b-description {
  font-size: 14px;
  font-weight: 400;
  color: #ffffff;
  line-height: 20px;
  padding: 0;
  margin: 0;
}
.b-tag {
  margin: 10px 0 0 0;
}
.bt-item {
  display: inline-block;
  padding: 4px 11px;
  background: #e1f5f5;
  border-radius: 4px;
  font-size: 12px;
  font-weight: 500;
  color: #2eafb4;
  line-height: 17px;
  margin: 0 8px;
}

.container {
  max-width: 1200px;
  padding: 0 20px;
  box-sizing: border-box;
  margin: 0 auto;
}

.c-head {
  display: grid;
  grid-template-columns: auto 416px;
  grid-column-gap: 24px;
  grid-row-gap: 24px;
  margin: 24px 0;
}
.ch-item {
  background: #ffffff;
  border-radius: 4px;
  padding: 24px;
  box-sizing: border-box;
}
.i-title {
  font-size: 20px;
  font-weight: 500;
  color: #333333;
  line-height: 28px;
  padding: 0;
  margin: 0 0 16px 0;
}
.i-more {
  font-size: 16px;
  font-weight: 400;
  color: #2eafb4;
  line-height: 22px;
  padding: 0;
  margin: 0;
}
.i-description {
  font-size: 16px;
  font-weight: 400;
  color: #333333;
  line-height: 22px;
  padding: 0;
  margin: 0;
}
.i-item {
  display: flex;
  .ii-name {
    flex-shrink: 0;
    font-size: 16px;
    font-weight: 400;
    color: #b2b2b2;
    line-height: 22px;
    padding: 0;
    margin: 0 16px 0 0;
  }
  .ii-link {
    font-size: 16px;
    font-weight: 500;
    color: #2eafb4;
    line-height: 22px;
    padding: 0;
    margin: 0;
  }
}
.ii-share {
  display: flex;
  a {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 32px;
    height: 32px;
    border-radius: 100%;
    overflow: hidden;
    background-color: #2eafb4;
    margin-left: 24px;
    &:nth-child(1) {
      margin-left: 0;
    }
  }
}
.ii-content,
.ii-text {
  font-size: 16px;
  font-weight: 400;
  color: #333333;
  line-height: 22px;
  padding: 0;
  margin: 0;
}

.item-link {
  .i-item {
    align-items: center;
  }
}

.proposals {
  background: #ffffff;
  border-radius: 4px;
  margin-bottom: 60px;
  padding: 24px;
  box-sizing: border-box;
}
.p-title {
  font-size: 20px;
  font-weight: 500;
  color: #333333;
  line-height: 28px;
  padding: 0;
  margin: 0;
  display: flex;
  align-items: center;
  .p-len {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 20px;
    height: 20px;
    border-radius: 100%;
    overflow: hidden;
    background: #b2b2b2;
    font-size: 12px;
    font-weight: 500;
    color: #ffffff;
    line-height: 17px;
    margin-left: 8px;
  }
}

.p-content {
  background: #f7f7f7;
  border-radius: 8px;
  border: 1px solid #dbdbdb;
  margin-top: 16px;
}
.pc-head {
  height: 60px;
  background: #ffffff;
  border-radius: 8px 8px 0px 0px;
  border-bottom: 1px solid #dbdbdb;
  display: flex;
  align-items: center;
  a {
    margin: 0 24px;
    font-size: 16px;
    font-weight: 500;
    color: #b2b2b2;
    line-height: 22px;
    &:hover {
      color: #333333;
    }
    &.active {
      font-size: 16px;
      font-weight: 500;
      color: #333333;
      line-height: 22px;
    }
  }
}
.pc-item {
  padding: 0;
  margin: 0;
  list-style: none;
}
.i-list {
  border-bottom: 1px solid #dbdbdb;
  padding: 16px 24px;
  background-color: #f7f7f7;
  &:nth-last-child(1) {
    border-bottom: none;
  }
  .il-tag {
    padding: 5px 20px;
    border-radius: 15px;
    background-color: #333;
    font-size: 14px;
    font-weight: 500;
    color: #ffffff;
    line-height: 20px;
    margin-right: 8px;

    &.active {
      background: #15bf59;
    }
    &.closed {
      background: #542de0;
    }
  }
  .il-title {
    font-size: 20px;
    font-weight: 500;
    color: #333333;
    line-height: 28px;
    padding: 0;
    margin: 0;
  }
  .il-text {
    margin-top: 8px;
font-size: 16px;
font-weight: 500;
color: #B2B2B2;
line-height: 22px;

  }
  .ilt-label {
        display: inline-block;
    padding: 0 7px;
    margin: 0 0 0 4px;
    font-size: 14px;
    font-weight: 500;
    height: 22px;
    line-height: 23px;
    border-radius: 2em;
    box-shadow: none;
    color: #B2B2B2;
    border:1px solid #B2B2B2;
  }
}
</style>
