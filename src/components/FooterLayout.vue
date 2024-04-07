<script setup>
</script>

<template>
  <div class="footer">
    <a href="/">
      <div class="menu-block">
        <img src="trade.svg" width="22" height="22" alt="trade-icon" />
        <div class="menu-text">
          Trade
        </div>
      </div>
    </a>
    <a href="/">
      <div class="menu-block">
        <img src="buy.svg" width="22" height="22" alt="buy-icon" />
        <div class="menu-text">
          Buy
        </div>
      </div>
    </a>
    <a href="/">
      <div class="menu-block">
        <img src="earn.svg" width="22" height="22" alt="earn-icon" />
        <div class="menu-text">
          Earn
        </div>
      </div>
    </a>
    <a href="/">
      <div class="menu-block">
        <img src="nft.svg" width="22" height="22" alt="nft-icon" />
        <div class="menu-text">
          NFT
        </div>
      </div>
    </a>
    <button class="menu-btn">
      <img src="ext.svg" width="22" height="22" alt="ext-icon" />
    </button>
    <button class="menu-btn">
      <img src="rabbit-bottom.svg" width="22" height="22" alt="rabbit-bottom-icon" />
      <span class="menu-text">Game</span>
    </button>
  </div>
</template>

<style scoped>
.footer {
  position: fixed;
  bottom: 0px;
  width: calc(100% - 16px);
  padding-top: 5px;
  padding-right: 8px;
  padding-left: 8px;
  background: #27262c;
  border-top: 1px solid #383241;
  display: flex;
  justify-content: space-around;
  z-index: 20;

  .menu-text {
    display: -webkit-box;
    overflow: hidden;
    -webkit-line-clamp: 1;
    -webkit-box-orient: vertical;
    user-select: none;
    color: #b8add2;
    line-height: 1.5;
    font-weight: 400;
    font-size: 10px;
  }

  a {
    display: block;
    border: 0px;
    background: transparent;
    cursor: pointer;
    height: 44px;
    padding: 0 12px;
    .menu-block {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100%;
      img {
        position: relative;
      }
    }
  }

  .menu-btn {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items:  center;
    border: 0px;
    background: transparent;
    cursor: pointer;
    height: 44px;
    padding: 4px 12px;
  }
}
</style>
