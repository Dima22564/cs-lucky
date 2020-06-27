<template>
  <main class="cs-lucky-main">
    <div class="cs-lucky-container">
      <div class="cs-lucky-row">
        <div class="cs-lucky-main--left">
          <div class="graph">
            <apex-charts :options="chartOptions" :series="series" />
          </div>

          <div class="players">
            <div class="players__item players__item_yellow">
              <div class="players__icon">
                <LayerIcon class="icon icon-30-w" />
              </div>
              <div class="players__text">
                <p class="num">
                  238.55
                </p>
                <p class="text">
                  Value
                </p>
              </div>
            </div>
            <div class="players__item players__item_pink">
              <div class="players__icon">
                <UserIcon class="icon icon-30-w" />
              </div>
              <div class="players__text">
                <p class="num">
                  238.55
                </p>
                <p class="text">
                  Value
                </p>
              </div>
            </div>
          </div>

          <div class="choose">
            <div class="choose__top">
              <span class="choose__num">$6.99</span>
            </div>

            <div class="choose__items">
              <div class="choose__item">
                <div class="choose__item-top">
                  <span class="choose__item-title">
                    FAMAS
                  </span>
                  <span class="choose__item-circle" />
                </div>

                <div class="choose__item-bottom">
                  <span class="text">Factorthrfhrtg</span>
                  <span class="num">$130.00</span>
                </div>
              </div>
              <div class="choose__item">
                <div class="choose__item-top">
                  <span class="choose__item-title">
                    FAMAS
                  </span>
                  <span class="choose__item-circle" />
                </div>

                <div class="choose__item-bottom">
                  <span class="text">Factorthrfhrtg</span>
                  <span class="num">$130.00</span>
                </div>
              </div>
              <div class="choose__item">
                <div class="choose__item-top">
                  <span class="choose__item-title">
                    FAMAS
                  </span>
                  <span class="choose__item-circle" />
                </div>

                <div class="choose__item-bottom">
                  <span class="text">Factorthrfhrtg</span>
                  <span class="num">$130.00</span>
                </div>
              </div>
              <div class="choose__item">
                <div class="choose__item-top">
                  <span class="choose__item-title">
                    FAMAS
                  </span>
                  <span class="choose__item-circle" />
                </div>

                <div class="choose__item-bottom">
                  <span class="text">Factorthrfhrtg</span>
                  <span class="num">$130.00</span>
                </div>
              </div>
              <div class="choose__item">
                <div class="choose__item-top">
                  <span class="choose__item-title">
                    FAMAS
                  </span>
                  <span class="choose__item-circle" />
                </div>

                <div class="choose__item-bottom">
                  <span class="text">Factorthrfhrtg</span>
                  <span class="num">$130.00</span>
                </div>
              </div>
              <div class="choose__item">
                <div class="choose__item-top">
                  <span class="choose__item-title">
                    FAMAS
                  </span>
                  <span class="choose__item-circle" />
                </div>

                <div class="choose__item-bottom">
                  <span class="text">Factorthrfhrtg</span>
                  <span class="num">$130.00</span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="cs-lucky-main--center">
          <div class="coeffs">
            <slick :options="sliderOptions">
              <div class="coeffs__item">
                <button class="coeffs__coeff">
                  1.58x
                </button>
              </div>
              <div class="coeffs__item">
                <button class="coeffs__coeff">
                  1.58x
                </button>
              </div>
              <div class="coeffs__item coeffs__item_green">
                <button class="coeffs__coeff coeffs__coeff_red">
                  1.58x
                </button>
              </div>
              <div class="coeffs__item">
                <button class="coeffs__coeff coeffs__coeff_green">
                  1.58x
                </button>
              </div>
              <div class="coeffs__item">
                <button class="coeffs__coeff coeffs__coeff_blue">
                  1.58x
                </button>
              </div>
              <div class="coeffs__item">
                <button class="coeffs__coeff coeffs__coeff_red">
                  1.58x
                </button>
              </div>
              <div class="coeffs__item">
                <button class="coeffs__coeff coeffs__coeff_red">
                  1.58x
                </button>
              </div>
              <div class="coeffs__item">
                <button class="coeffs__coeff coeffs__coeff_red">
                  1.58x
                </button>
              </div>
              <div class="coeffs__item">
                <button class="coeffs__coeff coeffs__coeff_red">
                  1.58x
                </button>
              </div>
            </slick>
          </div>

          <div class="history__con">
            <div class="history__bg" />
            <div class="history">
              <History
                :cost="12.2"
                :cost2="15.2"
                :coeff="2.30"
                :items="['sddsf', 'sdfsdf', 'dfrf', 'fergfe']"
                avatar="df"
              />
              <History
                :cost="12.2"
                :cost2="15.2"
                :coeff="2.30"
                :items="['sddsf']"
                avatar="df"
              />
              <History
                :cost="12.2"
                :cost2="15.2"
                :coeff="2.30"
                :items="['sddsf', 'sdfsdf', 'dfrf', 'fergfe']"
                avatar="df"
              />
            </div>
          </div>
        </div>

        <Chat />
      </div>
    </div>
  </main>
</template>

<script>
import LayerIcon from 'vue-material-design-icons/Layers.vue'
import UserIcon from 'vue-material-design-icons/Account.vue'
import Chat from '../components/Chat'
import History from '../components/History'
export default {
  layout: 'default',
  components: {
    LayerIcon,
    UserIcon,
    Chat,
    History
  },
  data () {
    return {
      sliderOptions: {
        slidesToShow: 7,
        slidesToScroll: 1,
        arrows: false,
        dots: false,
        variableWidth: true,
        infinite: false
      },
      series: [{
        name: 'series1',
        data: [1, 3, 10, 5]
      }],
      chartOptions: {
        chart: {
          type: 'area',
          // height: 350,
          zoom: {
            enabled: false
          }
        },
        dataLabels: {
          enabled: false,
          style: {
            colors: ['rgba(224, 224, 255, 0.4)']
          }
        },
        stroke: {
          curve: 'straight',
          colors: ['#ffaa00']
        },
        xaxis: {
          type: 'datetime',
          categories: [1991, 1992, 1993, 1994],
          axisTicks: {
            show: false
          },
          axisBorder: {
            show: false
          }
        },
        yaxis: {
          labels: {
            style: {
              colors: ['rgba(224, 224, 255, 0.4)', 'rgba(224, 224, 255, 0.4)', 'rgba(224, 224, 255, 0.4)', 'rgba(224, 224, 255, 0.4)', 'rgba(224, 224, 255, 0.4)', 'rgba(224, 224, 255, 0.4)', 'rgba(224, 224, 255, 0.4)', 'rgba(224, 224, 255, 0.4)', 'rgba(224, 224, 255, 0.4)', 'rgba(224, 224, 255, 0.4)', 'rgba(224, 224, 255, 0.4)', 'rgba(224, 224, 255, 0.4)', 'rgba(224, 224, 255, 0.4)', 'rgba(224, 224, 255, 0.4)', 'rgba(224, 224, 255, 0.4)', 'rgba(224, 224, 255, 0.4)', 'rgba(224, 224, 255, 0.4)', 'rgba(224, 224, 255, 0.4)']
            }
          }
        },
        markers: {
          size: 0,
          strokeColor: '#ffaa00',
          colors: 'rgba(224, 224, 255, 0.4)'
        },
        colors: ['#ffaa00'],
        fill: {
          type: 'gradient',
          colors: '#ffaa00',
          gradient: {
            opacityFrom: 0.8,
            opacityTo: 0.1
          }
        },
        grid: {
          row: {
            colors: ['rgba(224, 224, 255, 0.1)']
          },
          column: {
            colors: ['rgba(224, 224, 255, 0.1)']
          }
        },
        tooltip: {
          enabled: false
        }
      }
    }
  }
}
</script>

<style lang="sass">
@import '../theme/_var'
.cs-lucky-main
  padding: 24px 0 0
  &--left
    max-width: 356px
    width: 100%
    flex-shrink: 0
  &--center
    padding: 0 24px
    width: calc(100% - 332px - 352px - 24px)
.apexcharts-toolbar
  display: none !important
.players
  display: flex
  justify-content: space-between
  margin-bottom: 24px
  .num
    @extend %font-18-24
    letter-spacing: -0.4px
    font-weight: bold
  .text
    @xtend %font-13-16
    color: $dark-white
  &__item
    width: calc(50% - 12px)
    color: $white
    padding: 12px 30px 12px 16px
    border-radius: 24px
    display: flex
    align-items: center
    justify-content: space-between
    &_yellow
      background: $main-gradient
      box-shadow: $main-shadow
    &_pink
      box-shadow: $secondary-shadow
      background: $secondary-gradient
  &__text
    margin-left: 16px
  &__icon
    width: 40px
    height: 40px
    flex-shrink: 0
    display: flex
    align-items: center
    justify-content: center
    border-radius: 12px
    +white(0.06, 'bg')

.choose
  padding: 24px
  background-image: $dark-gradient
  box-shadow: $dark-shadow
  border-radius: 24px
  height: calc(100vh - 482px)
  overflow: hidden
  &__top
    display: flex
    align-items: center
    justify-content: space-between
    margin-bottom: 24px
  &__num
    @extend %font-18-24
    letter-spacing: -0.4px
    font-weight: bold
  &__items
    display: flex
    justify-content: space-between
    flex-wrap: wrap
    overflow-y: auto
    height: calc(100% - 45px)
    margin-right: -24px
    padding-right: 24px
    background: $dark-gradient
  &__item
    width: calc(50% - 12px)
    border-radius: 12px
    background-color: rgba(224, 224, 255, 0.02)
    margin-bottom: 24px
    &-top
      display: flex
      align-items: center
      justify-content: space-between
      margin-bottom: 12px
      padding: 12px
    &-title
      @extend %font-10-12
    &-circle
      width: 12px
      height: 12px
      border-radius: 50%
      background: #c32de1
    &-bottom
      display: flex
      align-items: center
      justify-content: space-between
      padding: 6px 12px
      @extend %font-10-12
      +white(0.4, 'c')
      .num
        margin-left: 12px
        @extend %font-13-16
        font-weight: bold
        color: $white
      .text
        overflow: hidden
        text-overflow: ellipsis

.coeffs
  background-image: linear-gradient(96deg, #2d2f33 1%, #272a2e 52%, #222529)
  border-radius: 24px
  padding: 12px
  margin-bottom: 24px
  box-shadow: $dark-shadow
  .slick-slide
    margin-right: 12px
  &__coeff
    @extend %btn-refresh
    font-size: 16px
    line-height: 24px
    padding: 10px 16px
    border-radius: 12px;
    border: solid 2px #c32de1;
    background-color: rgba(195, 45, 225, 0.06)
    color: $white
    font-weight: bold
    &_red
      border: solid 2px #ff00aa;
      background-color: rgba(255, 0, 170, 0.06)
    &_green
      border: solid 2px #00ffaa;
      background-color: rgba(0, 255, 170, 0.06)
    &_blue
      border: solid 2px #00bbff;
      background-color: rgba(0, 187, 255, 0.06)

.history
  height: calc(100vh - 72px - 48px - 120px - 228px)
  overflow-y: auto
  margin: 0 0 0 -43px
  padding: 0 0 0 43px
  position: relative
  &__con
    position: relative
  &__bg
    background-image: linear-gradient(to bottom, rgba(33, 36, 41, 0), #212429)
    position: absolute
    bottom: 0
    left: 0
    width: 100%
    height: 128px
    z-index: 5

.graph
  background-image: linear-gradient(124deg, #2d2f33 1%, #272a2e 52%, #222529 100%)
  border-radius: 24px
  margin-bottom: 24px
  box-shadow: $dark-shadow
  height: 215px
</style>
