<script setup>
import { onUnmounted, ref} from 'vue'

const changeSlide = (slide) => {
  swiperNumber.value = slide
}

const swiperNumber = ref(1)
const betTimer = setInterval(() => {
  if (swiperNumber.value <= 2) {
    swiperNumber.value++
  } else {
    swiperNumber.value = 1
  }
}, 5000)

onUnmounted(() => clearInterval(betTimer))
</script>

<template>
  <div class="home-page">
    <div class="home-container">
      <div class="container-block">
        <div class="landing-block">
          <div class="landing-image">
            <div class="image-container">
              <div class="swiper-wrapper">

<!--                Block 1-->
                <div :class="swiperNumber === 1 ? 'swiper-active' : 'swiper-hidden'" class="swiper-block">
                  <div class="swiper-layout swiper-bg-1">
                    <div class="layout-left">
                      <div class="layout-left-top">
                        <div class="top-title">
                          <img src="/title-icon-1.svg" width="20" height="20" alt="title-icon-1.svg" />
                          <div class="title-text">
                            PancakeSwap
                          </div>
                        </div>
                        <div class="top-center">
                          <div class="center-title">
                            Stake CAKE - up to 27.54% APR !
                          </div>
                        </div>
                      </div>
                      <div class="layout-left-bottom">
                        <a href="/" class="bottom-stake">
                          <div class="stake-container no-wrap">
                            Stake CAKE
                            <img src="/stake-icon.svg" width="20" class="stake-icon" alt="stake-icon" />
                          </div>
                        </a>
                        <a href="/" class="bottom-stake">
                          <div class="stake-container">
                            Learn More
                            <img src="/explore-icon.svg" width="20" class="stake-icon" alt="explore-icon" />
                          </div>
                        </a>
                      </div>
                    </div>
                    <div class="layout-right">
                      <div class="right-container">
                        <div class="right-container-block">
                          <div class="right-image image-right-slide-1" />
                        </div>
                        <div class="right-absolute-1">
                          <div class="right-floating-item-1" />
                        </div>
                      </div>
                    </div>
                  </div>
                </div>

<!--                Block 2-->
                <div :class="swiperNumber === 2 ? 'swiper-active' : 'swiper-hidden'" class="swiper-block">
                  <div class="swiper-layout swiper-bg-2">
                    <div class="layout-left">
                      <div class="layout-left-top">
                        <div class="top-title">
                          <img src="/title-icon-1.svg" width="20" height="20" alt="title-icon-1.svg" />
                          <div class="title-text">
                            PancakeSwap
                          </div>
                        </div>
                        <div class="top-center">
                          <div class="stake-wbnb">
                            Stake WBNB, Win Combo Rewards!
                          </div>
                        </div>
                      </div>
                      <div class="layout-left-bottom">
                        <a href="/" class="bottom-stake-2">
                          <div class="stake-container-2 no-wrap">
                            Stake Now
                            <img src="/arrow-right.svg" width="20" class="stake-icon" alt="stake-icon" />
                          </div>
                        </a>
                        <a href="/" class="bottom-stake-2">
                          <div class="stake-container-2 no-wrap">
                            Learn More
                            <img src="/explore-icon-2.svg" width="20" class="stake-icon" alt="explore-icon" />
                          </div>
                        </a>
                      </div>
                    </div>
                    <div class="layout-right">
                      <div class="right-container">
                        <div class="right-container-block">
                          <div class="right-image image-right-slide-2" />
                        </div>
                        <div class="right-absolute-2">
                          <div class="right-floating-item-2" />
                        </div>
                      </div>
                    </div>
                  </div>
                </div>

<!--                Block 3-->
                <div :class="swiperNumber === 3 ? 'swiper-active' : 'swiper-hidden'" class="swiper-block">
                  <div class="swiper-layout swiper-bg-3">
                    <div class="layout-left">
                      <div class="layout-left-top">
                        <div class="top-title">
                          <img src="/title-icon-1.svg" width="20" height="20" alt="title-icon-1.svg" />
                          <div class="title-text">
                            PancakeSwap
                          </div>
                        </div>
                        <div class="top-center">
                          <div class="stake-wbnb">
                            Introducing PancakeSwap v4
                          </div>
                        </div>
                      </div>
                      <div class="layout-left-bottom">
                        <a href="/" class="bottom-stake-3">
                          <div class="stake-container-2 no-wrap">
                            Whitepaper
                            <img src="/explore-icon-2.svg" width="20" class="stake-icon" alt="explore-icon" />
                          </div>
                        </a>
                        <a href="/" class="bottom-stake-3-1">
                          <div class="stake-container-3 no-wrap">
                            Build
                            <img src="/explore-icon.svg" width="20" class="stake-icon" alt="explore-icon" />
                          </div>
                        </a>
                      </div>
                    </div>
                    <div class="layout-right">
                      <div class="right-container">
                        <div class="right-container-block">
                          <div class="right-image image-right-slide-3" />
                        </div>
                        <div class="right-absolute-1">
                          <div class="right-floating-item-3" />
                        </div>
                      </div>
                    </div>
                  </div>
                </div>

              </div>

              <div class="swiper-pagination">
                <span v-for="i in 3" :key="i" :class="{ 'swiper-pagination-bullet-active' : swiperNumber === i }" class="swiper-pagination-bullet" @click="changeSlide(i)" />
              </div>
            </div>
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
                <br class="landing-br" />
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
              <img src="/mshk-lottie1.gif" alt="lottie-gif">
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
      justify-content: center;
      position: relative;
      margin-bottom: 24px;
      img {
        width: 375px;
        height: 375px;
        @media screen and (min-width: 576px) {
          width: 500px;
          height: 500px;
          transform-origin: center center;
        }
      }
    }
  }

  .landing-image {
    position: relative;
    height: 179px;
    max-width: 100%;
    box-sizing: border-box;
    margin-top: 0px;
    margin-bottom: 0px;
    &::before {
      content: "";
      border-radius: 32px;
      position: absolute;
      inset: 0px;
      //background: -webkit-linear-gradient(top, rgb(118, 69, 217) 0%, rgb(69, 42, 122) 100%);
    }

    .image-container {
      position: relative;
      overflow: visible;
      opacity: 0;
      animation: 0.3s ease-in-out 0.7s 1 normal forwards running fGxCd;

      touch-action: pan-y;
      margin-left: auto;
      margin-right: auto;
      list-style: none;
      padding: 0;
      z-index: 1;
      display: block;
    }

    .swiper-wrapper {
      position: relative;
      width: 100%;
      height: 100%;
      z-index: 1;
      display: flex;
      transition-property: transform;
      transition-timing-function: ease-in;
      box-sizing: content-box;
      transform: translateZ(0);
    }

    .swiper-block {
      padding: 0px;
      height: auto;
      width: 100%;
      opacity: 1;
      transform: translate3d(0px, 0px, 0px);
      transition-duration: 500ms;
      overflow: visible;
      backface-visibility: hidden;
      flex-shrink: 0;
      position: relative;
      transition-property: transform;
      display: block;
    }

    .swiper-layout {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      border-radius: 32px;
      max-width: 100%;
      height: 192px;
    }

    .layout-left {
      z-index: 2;
      width: 50%;
      position: relative;
      padding: 22px 0px 22px 22px;
      gap: 6px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    .layout-left-top {
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      gap: 12px;
      width: 100%;
    }

    .top-title {
      gap: 4px;
      display: flex;
      flex-direction: row;
      justify-content: flex-start;
      align-items: center;
      width: 100%;
    }

    .title-text {
      color: rgb(9, 9, 9);
      font-weight: 600;
      font-size: 16px;
      line-height: 20px;
    }

    .top-center {
      width: 100%;
      gap: 6px;
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      max-width: 155px;
      @media all and (min-width: 450px) {
        min-width: unset;
      }
    }

    .center-title {
      color: rgb(255, 178, 55);
      font-weight: 800;
      font-size: calc(20px);
      line-height: calc(21.4286px);
      text-shadow: rgb(118, 69, 217) -2px 2px 0px, rgb(118, 69, 217) 2px 2px 0px, rgb(118, 69, 217) 2px -2px 0px, rgb(118, 69, 217) -2px -2px 0px;
    }

    .layout-left-bottom {
      gap: 8px;
      display: flex;
    }

    .stake-container {
      display: flex;
      align-items: center;
      color: black;
      font-size: 14px;
      line-height: 16px;
    }

    .stake-container-2 {
      display: flex;
      align-items: center;
      color: white;
      font-size: 14px;
      line-height: 16px;
      font-weight: 500;
    }

    .stake-container-3 {
      display: flex;
      align-items: center;
      color: #000;
      font-size: 14px;
      line-height: 16px;
      font-weight: 500;
    }

    .stake-icon {
      margin-left: 4px;
      align-self: center;
      flex-shrink: 0;
    }
  }

  .layout-right {
    z-index: 1;
    position: relative;
    width: 50%;
    display: flex;
  }

  .right-container {
    position: absolute;
    width: 100%;
    left: 0px;
    bottom: 0px;
    height: 122%;
    overflow: hidden;
    border-radius: 0px 0px 32px;
  }

  .right-container-block {
    left: 0;
    bottom: 0;
    position: absolute;
  }

  .right-image {
    background-size: cover;
    width: 221px;
    height: 182px;
  }

  .right-absolute-1 {
    left: 0px;
    position: absolute;
    top: 30%;
    animation: 2.5s ease-in-out 0s infinite normal none running gyagOf;
  }

  .right-absolute-2 {
    left: 3%;
    top: 10%;
    position: absolute;
    animation: 2.5s ease-in-out 0s infinite normal none running gyagOf;
  }

  .stake-wbnb {
    color: rgb(118, 69, 217);
    font-weight: 800;
    font-size: calc(20px);
    line-height: calc(21.4286px);
    text-shadow: rgb(255, 255, 255) -2px 2px 0px, rgb(255, 255, 255) 2px 2px 0px, rgb(255, 255, 255) 2px -2px 0px, rgb(255, 255, 255) -2px -2px 0px;
  }

  // Different
  .swiper-bg-1 {
    background: radial-gradient(100.66% 178.94% at 26.19% 58.89%, rgb(83, 222, 233) 0%, rgb(31, 199, 212) 69.43%, rgb(0, 152, 161) 100%) center center / cover;
  }

  .swiper-bg-2 {
    background: linear-gradient(64deg, rgba(214, 126, 10, 0.26) 44.37%, rgba(255, 235, 55, 0) 102.8%) center center / cover, radial-gradient(113.12% 140.14% at 26.47% 0%, rgb(245, 223, 142) 0%, rgb(252, 198, 49) 33.21%, rgb(255, 157, 0) 79.02%);
  }

  .swiper-bg-3 {
    background: radial-gradient(112.67% 197.53% at 30.75% 3.72%, rgb(154, 237, 255) 0%, rgb(204, 194, 254) 76.19%, rgb(198, 163, 255) 100%) center center / cover, linear-gradient(rgba(231, 253, 255, 0.2) 0%, rgba(242, 241, 255, 0.2) 100%);
  }

  .bottom-stake {
    padding: 4px 0px;
    display: flex;
    font-weight: 600;
    align-items: center;
    width: fit-content;
    color: black;
    line-height: 1.5;
    font-size: 16px;
  }

  .bottom-stake-2 {
    height: 33px;
    border-radius: 12px;
    box-shadow: rgba(0, 0, 0, 0.2) 0px -2px 0px inset;
    padding: 0px 12px;
    position: relative;
    align-items: center;
    border: 0px;
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
    background-color: #1fc7d4;
    color: #191326;
  }

  .bottom-stake-3 {
    height: 33px;
    border-radius: 12px;
    box-shadow: rgba(0, 0, 0, 0.2) 0px -2px 0px inset;
    padding: 0px 12px;
    position: relative;
    align-items: center;
    border: 0px;
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
    background-color: #a881fc;
    color: #191326;
  }

  .bottom-stake-3-1 {
    height: 33px;
    border-radius: 12px;
    padding: 0px 12px;
    position: relative;
    align-items: center;
    border: 0px;
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
    color: #191326;
  }

  .image-right-slide-1 {
    background-image: url('/public/slide-1.png');
  }

  .image-right-slide-2 {
    background-image: url('/public/slide-2.png');
  }

  .image-right-slide-3 {
    background-image: url('/public/slide-3.png');
  }

  .right-floating-item-1 {
    background-image: url('/public/floating-item.png');
    background-size: cover;
    width: 74.25px;
    height: 74.25px;
  }

  .right-floating-item-2 {
    background-image: url('/public/floating-item-2.png');
    background-size: cover;
    width: 67.5px;
    height: 67.5px;
  }

  .right-floating-item-3 {
    background-image: url('/public/floating-item-3.png');
    background-size: cover;
    width: 74.25px;
    height: 74.25px;
  }
}

.no-wrap {
  white-space: nowrap
}

.swiper-hidden {
  opacity: 0;
  display: none !important;
  transition: all 0.3s ease-in-out;
}

.swiper-active {
  opacity: 1;
  display: block !important;
  transition: all 0.3s ease-in-out;
}

.swiper-pagination {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  justify-content: center;
  width: 108px;
  bottom: 12px;
  text-align: center;
  transition: opacity .3s;
  z-index: 10;
}

.swiper-pagination-bullet {
  background-color: white;
  flex-basis: 108px;
  border-radius: 0px;
  margin: 0px !important;
  cursor: pointer;
  height: 8px;
  width: 12px;
  opacity: 0.2;

  &:first-child {
    border-radius: 4px 0px 0px 4px;
  }

  &:last-child {
    border-radius: 0px 4px 4px 0px;
  }
}

.swiper-pagination-bullet-active {
  opacity: 1;
}

.landing-br {
  display: block;
  @media all and (min-width: 576px) {
    display: none;
  }
}

@keyframes gyagOf {
  0% {
    transform: translate(0px, 0px);
  }
  50% {
    transform: translate(-5px, 5px);
  }
  100% {
    transform: translate(0px, 0px);
  }
}

@keyframes fGxCd {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>