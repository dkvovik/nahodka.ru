<template>
  <header class="container-fluid">
    <div class="row">
      <div class="col-12 header-wrapper">
        <div class="overlay"></div>
        <div class="container header-content mt-2 mt-sm-5">
          <div class="row">
            <nav class="col-12 navbar justify-content-start align-items-baseline">
              <div class="logo mr-3 mr-sm-4"><a href="#" class="logo__link">НАХОДКА</a></div>
              <div class="location">
                <svg width="22" height="22" class="mr-1 mr-sm-2 svg-geo"
                     viewBox="0 0 190 247" version="1.1"
                     xmlns="http://www.w3.org/2000/svg">
                  <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                    <g id="Artboard">
                      <g id="SVG-Layer" transform="translate(-31.000000, -5.000000)">
                        <g id="Group">
                          <polygon id="Shape" points="0 252 0 0 252 0 252 252"></polygon>
                          <polygon id="Shape-Copy" points="0 252 0 0 252 0 252 252"></polygon>
                          <g transform="translate(31.000000, 5.000000)" fill="#FFFFFF" fill-rule="nonzero" id="Layer_3">
                            <g>
                              <path
                                  d="M95,0.25 C141.2,0.25 189.416,37.01575 189.5,89.5 C189.59975,152.5315 95,247 95,247 C95,247 0.4055,152.40025 0.5,89.5 C0.57875,36.937 48.8,0.25 95,0.25 Z M95.4999292,152.256668 C128.634929,152.256668 155.499929,125.391668 155.499929,92.256668 C155.499929,59.121668 128.634929,32.256668 95.4999292,32.256668 C62.3649292,32.256668 35.4999292,59.121668 35.4999292,92.256668 C35.4999292,125.391668 62.3649292,152.256668 95.4999292,152.256668 Z"
                                  id="Shape"></path>
                            </g>
                          </g>
                        </g>
                      </g>
                    </g>
                  </g>
                </svg>
                <b-btn id="changeCity" class="changeCity">{{ selectedCity }}</b-btn>
                <b-popover target="changeCity" triggers="click blur"
                           class="b-popover" placement="bottom">
                  <a :href="option.value" v-for="option in options"
                     v-if="option.text !== selectedCity">{{ option.text }}<br></a>
                </b-popover>
              </div>
            </nav>
            <div class="w-100"></div>
            <div class="col-12 promo">
              <h1 class="title title color-white">Аренда авто<br>под такси</h1>
              <p class="subtitle color-white">Хочешь работать в такси, но нет личной машины? Возьми автомобиль в аренду</p>
              <button class="btn">УЗНАТЬ ПОДРОБНЕЕ</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data () {
    return {
      selectedCity: 'Москва',
      options: [
        {value: 'moscow', text: 'Москва'},
        {value: 'kirov', text: 'Киров'},
        {value: 'tula', text: 'Тула'},
      ],
    }
  },
}
</script>

<style scoped lang="scss">
.header-wrapper {
  position: relative;
  min-height: calc(100vh - 20px);
  background: url('../assets/images/bg-header.jpg');
  background-size: cover;
  @media (max-width: 1199px) {
    background-position-x: -300px;
  }
  @media (max-width: 991px) {
    background-position-x: -400px;
  }
  @media (max-width: 575px) {
    background-position-x: -300px;
  }
}

.changeCity {
  text-transform: none;
  cursor: pointer;
  background: none;
  color: rgb(255, 255, 255);
  border: none;
  padding: 0;
  width: auto;
  @media (max-width: 575px) {
    font-size: 0.6667rem;
  }

  &:focus {
    box-shadow: none;
  }
}

.header-content {
  .logo__link {
    font-weight: bold;
    text-transform: uppercase;
  }
  .navbar {
    .location {
      display: flex;
      align-items: center;
    }
    .svg-geo {
      width: 22px;
      height: 22px;

      @media (max-width: 575px) {
        width: 0.5833rem;
        height: 0.5833rem;
      }
    }
  }
  .promo {
    margin-top: 80px;
    max-width: 550px;
  }
}
</style>

<style lang="scss">
.popover-cars {
  .popover-body {
    position: relative;
    padding: 45px;
    background-color: #ffc61a;
  }
  .arrow::after {
    border-top-color: #ffc61a;
  }
  .close {
    position: absolute;
    top: 0;
    right: 10px;
  }
}
</style>
