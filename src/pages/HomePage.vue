<script setup>
</script>

<template>
  <div class="home-page">
    <div class="home-container">
      <div class="container-block">
        <div class="landing-block">
          <div class="landing-image">
          </div>
          <div class="landing-body">
            <div class="body-text">
              <div class="text-title">
                <div class="text-title--first">
                  Everyone's
                </div>
                <div class="text-title--second">
                  Favorite
                </div>
                <br />
                <div class="text-title--first">
                  DEX
                </div>
              </div>
              <div class="text-description">
                Trade, earn, and own crypto on the all-in-one multichain DEX
              </div>
              <div class="text-action">
                <button class="action-left">Connect Wallet</button>
                <button class="action-right">Trade Now</button>
              </div>
            </div>
            <div class="body-image">

            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.home-page {
  position: relative;
  display: flex;
  max-width: 100vw;
  margin-top: 57px;

  .home-container {
    flex-grow: 1;
    transition: margin-top 0.2s ease 0s, margin-left 0.2s cubic-bezier(0.4, 0, 0.2, 1) 0s;
    transform: translate3d(0px, 0px, 0px);
    max-width: 100%;
  }

  .container-block {
    position: relative;
    flex-direction: column;
    align-items: center;
    z-index: 1;
    padding-bottom: 48px;
    padding-top: 16px;
    display: flex;
    background: radial-gradient(103.12% 50% at 50% 50%, #21193a 0%, #191326 100%);
  }

  .landing-block {
    margin: 0px;
    width: calc(100% - 32px);
    overflow: visible;
    padding: 16px;
    min-height: auto;
    max-width: 1200px;
  }

  .landing-image {
    //position: relative;
    //height: 179px;
    //max-width: 100%;
    //box-sizing: border-box;
    //margin-top: 0px;
    //margin-bottom: 0px;
  }

  .landing-body {
    display: flex;
    flex-direction: column-reverse;
    align-items: center;
    justify-content: center;
    padding-left: 0px;
    position: relative;
    margin-top: 50px;

    .body-text {
      display: flex;
      flex: 1 1 0%;
      flex-direction: column;

      .text-title {
        color: #f4eeff;
        font-weight: 400;
        line-height: 1.5;
        padding-right: 0px;
        margin-bottom: 16px;
        text-align: center;
        font-size: 16px;
        &--first {
          color: #f4eeff;
          margin-right: 8px;
          line-height: 110%;
          font-weight: 600;
          font-size: 32px;
          display: inline-block;
        }
        &--second {
          color: #a881fc;
          margin-right: 8px;
          line-height: 110%;
          font-weight: 600;
          font-size: 32px;
          display: inline-block;
        }
      }

      .text-description {
        font-size: 20px;
        color: rgb(184, 173, 210);
        margin-bottom: 24px;
        text-align: center;
        line-height: 110%;
        font-weight: 600;
        max-width: 600px;
      }

      .text-action {
        display: flex;
        justify-content: center;

        .action-left {
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
          height: 48px;
          padding: 0px 24px;
          background-color: #1fc7d4;
          color: #191326;
          margin-right: 8px;
        }

        .action-right {
          position: relative;
          align-items: center;
          border-radius: 16px;
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
          height: 48px;
          padding: 0px 24px;
          background-color: transparent;
          border-width: 2px;
          border-style: solid;
          border-image: initial;
          border-color: #1fc7d4;
          box-shadow: none;
          color: #1fc7d4;
        }
      }
    }

    .body-image {
      display: flex;
      height: 100%;
      width: 100%;
      position: relative;
      margin-bottom: 24px;
    }
  }
}
</style>