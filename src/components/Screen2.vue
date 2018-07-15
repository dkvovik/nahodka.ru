<template>
  <b-container fluid class="provide-wrapper">
    <b-row>
      <b-container>
        <b-row>
          <b-col cols="12">
            <h2 class="title color-grey text-center mb-3 mb-sm-5">Мы предоставим</h2>
          </b-col>

          <div class="w-100 mb-4"></div>

          <b-col cols="12" sm="6" lg="3" class="provide provide-cars text-center mb-3 mb-lg-0" id="cars">
            <img class="provide-icon mb-3" src="../assets/images/car.png"
                 srcset="../assets/images/car@2x.png 2x, ../assets/images/car@3x.png 3x">
            <p class="provide-text text-center color-grey">Автопарк из разных марок машин не старше 2-х лет</p>
            <b-popover target="cars" container="cars" placement="top" triggers="hover"
                       :delay="{show: 100, hide: 100}">
              <button type="button" class="close" aria-label="Close" @click="onHidePopover">
                <span aria-hidden="true">&times;</span>
              </button>

              <vueper-slides autoplay :bullets="false">
                <vueper-slide v-for="(slide, i) in slides" :key="i"
                              :content="slide.content"
                >
                </vueper-slide>
              </vueper-slides>

            </b-popover>
          </b-col>


          <b-col cols="12" sm="6" lg="3" class="provide text-center mb-3 mb-lg-0" id="connect">
            <img class="provide-icon mb-3" src="../assets/images/taxi.png"
                 srcset="../assets/images/taxi@2x.png 2x, ../assets/images/taxi@3x.png 3x">
            <p class="provide-text text-center color-grey">Подключение к Я.Такси и Uber</p>
            <b-popover target="connect" triggers="hover" placement="top" container="connect"
                       :delay="{show: 100, hide: 100}">
              <button type="button" class="close" aria-label="Close" @click="onHidePopover">
                <span aria-hidden="true">&times;</span>
              </button>
              <p class="text">Мы предоставляем подключение к сервисам Я.Такси и Uber</p>
            </b-popover>
          </b-col>

          <b-col cols="12" sm="6" lg="3" class="provide text-center mb-3 mb-lg-0" id="maintenance">
            <img class="provide-icon mb-3" src="../assets/images/tech.png"
                 srcset="../assets/images/tech@2x.png 2x, ../assets/images/tech@3x.png 3x">
            <p class="provide-text color-grey">Техническое обслуживание</p>
            <b-popover target="maintenance" triggers="hover" placement="top" container="maintenance"
                       :delay="{show: 100, hide: 100}">
              <button type="button" class="close" aria-label="Close" @click="onHidePopover">
                <span aria-hidden="true">&times;</span>
              </button>
              <p class="text">Все вопросы технического обслуживания берем на себя</p>
            </b-popover>
          </b-col>

          <b-col cols="12" sm="6" lg="3" class="provide text-center" id="contract">
            <img class="provide-icon mb-3" src="../assets/images/doc.png"
                 srcset="../assets/images/doc@2x.png 2x, ../assets/images/doc@3x.png 3x">
            <p class="provide-text text-center color-grey">Договор</p>
            <b-popover target="contract" triggers="hover" placement="top" container="contract"
                       :delay="{show: 100, hide: 100}">
              <button type="button" class="close" aria-label="Close" @click="onHidePopover">
                <span aria-hidden="true">&times;</span>
              </button>
              <p class="text">Аренда авто будет официально оформлена</p>
            </b-popover>
          </b-col>
        </b-row>
      </b-container>
    </b-row>
  </b-container>
</template>

<script>
import {VueperSlides, VueperSlide} from 'vueperslides'

export default {
  components: {VueperSlides, VueperSlide},
  data () {
    return {
      slides: [
        {
          content: `
            <div class="slider-item">
              <div class="slider-img">
                <img src="/dist/slide1.jpg" alt="">
              </div>
              <div class="slider-info pl-3 align-content-center">
                <div class="slider-title">Kia Rio</div>
                <div class="slider-text">
                    <p class="mb-0"><strong>Год выпуска:</strong> 2015</p>
                    <p class="mb-0"><strong>Пробег:</strong> 30 000 км</p>
                </div>
              </div>
            </div>`
        },
        {
          content: `
            <div class="slider-item">
              <div class="slider-img">
                <img src="/dist/slide2.jpg" alt="">
              </div>
              <div class="slider-info pl-3 align-content-center">
                <div class="slider-title">Volkswagen Polo</div>
                <div class="slider-text">
                    <p class="mb-0"><strong>Год выпуска:</strong> 2015</p>
                    <p class="mb-0"><strong>Пробег:</strong> 30 000 км</p>
                </div>
              </div>
            </div>`
        },
        {
          content: `
            <div class="slider-item">
              <div class="slider-img">
                <img src="/dist/slide3.jpg" alt="">
              </div>
              <div class="slider-info pl-3 align-content-center">
                <div class="slider-title">Hyundai Solaris</div>
                <div class="slider-text">
                    <p class="mb-0"><strong>Год выпуска:</strong> 2015</p>
                    <p class="mb-0"><strong>Пробег:</strong> 30 000 км</p>
                </div>
              </div>
            </div>`
        }
      ],
      show: false,
    }
  },
  methods: {
    onHidePopover () {
      this.$root.$emit('bv::hide::popover')
    }
  }
}
</script>

<style scoped lang="scss">
.provide-wrapper {
  padding-top: 125px;
  padding-bottom: 125px;
  background: url(../assets/images/bg-provide.png) bottom repeat-x;
  background-size: 100% 70%;
  @media (max-width: 768px) {
    background-size: cover;
  }
  @media (max-width: 574px) {
    padding-top: 75px;
    padding-bottom: 75px;
  }

  .provide-icon {
    height: 83px;
  }
}

.provide /deep/ {
  .popover {
    width: 380px;
    max-width: 90vw;
    border-radius: 0;
  }
  .popover-body {
    position: relative;
    padding: 45px;
    background-color: #ffc61a;
  }
  .bs-popover-bottom .arrow::after {
    border-bottom-color: #ffc61a;
  }
  .arrow::after {
    border-top-color: #ffc61a;
  }
  .close {
    position: absolute;
    top: 5px;
    right: 15px;
    font-weight: 100;

    &:focus {
      outline: none;
    }
  }
  .text {
    color: #161616;
    font-size: 0.9167rem;
    margin-bottom: 0;
    text-align: center;

    @media (max-width: 767px) {
      font-size: 0.6667rem;
    }
  }
}

.provide-cars /deep/ {
  .popover{
    width: 565px;
    max-width: 95vw;

    .popover-body {
      position: relative;
      padding: 60px 0 45px 0;
      background-color: #ffc61a;
      @media (max-width: 575px) {
        padding: 20px 0 15px 0;
      }
    }
  }
}
</style>