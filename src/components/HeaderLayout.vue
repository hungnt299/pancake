<script setup>
</script>

<template>
  <div class="header-layout">
    <div class="header">
      <img src="/rabbit-icon.svg" width="32" height="32" alt="rabbit-icon" />
      <div class="header-right">
        <div class="header-action">
          <img src="/language.svg" width="24" height="24" alt="language-icon" />
          <img src="/setting.svg" width="24" height="24" alt="setting-icon" />
          <img src="/ring.svg" width="24" height="24" alt="ring-icon" />
        </div>
        <div class="header-network">
          <img src="/network.png" width="32" height="32" alt="network-icon" />
          <div class="header-title">BNB</div>
          <img src="/move-down.svg" width="24" height="24" alt="move-down-icon" />
        </div>
        <div class="connect-btn">
          <div>Connect</div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.header-layout {
  position: fixed;
  top: 0px;
  left: 0px;
  transition: top 0.2s ease 0s;
  height: 56px;
  width: 100%;
  z-index: 20;

  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: calc(100% - 32px);
    height: 56px;
    background-color: #27262c;
    border-bottom: 1px solid #383241;
    transform: translate3d(0px, 0px, 0px);
    padding-left: 16px;
    padding-right: 16px;
  }

  .header-right {
    display: flex;
    height: 100%;
    align-items: center;
  }

  .header-action {
    display: flex;
    height: 100%;
    align-items: center;
    gap: 20px;
  }

  .header-network {
    align-items: center;
    background-color: #353547;
    border-radius: 16px;
    box-shadow: rgba(0, 0, 0, 0.1) 0px -2px 0px inset;
    cursor: pointer;
    display: inline-flex;
    height: 32px;
    padding-right: 8px;
    margin-right: 8px;
    margin-left: 20px;
    position: relative;
    &:hover {
      opacity: 0.65;
    }

    .header-title {
      color: #f4eeff;
      display: none;
      font-weight: 600;

      @media screen and (min-width: 576px) {
        display: block;
        margin-left: 8px;
        margin-right: 4px;
      }
    }
  }

  .connect-btn {
    position: relative;
    align-items: center;
    border: 0px;
    border-radius: 16px;
    box-shadow: rgba(14, 14, 44, 0.4) 0px -1px 0px 0px inset;
    cursor: pointer;
    display: inline-flex;
    font-family: inherit;
    font-size: 16px;
    font-weight: 600;
    justify-content: center;
    letter-spacing: 0.03em;
    line-height: 1;
    opacity: 1;
    outline: 0px;
    transition: background-color 0.2s ease 0s, opacity 0.2s ease 0s;
    height: 32px;
    padding: 0px 16px;
    background-color: #1fc7d4;
    color: #191326;
  }
}
</style>