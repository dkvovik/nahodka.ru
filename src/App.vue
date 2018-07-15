<template>
  <div id="app">
    <screen1></screen1>
    <div class="separator"></div>
    <screen2></screen2>
    <screen3></screen3>
  </div>
</template>

<script>
import Screen1 from './components/Screen1.vue'
import Screen2 from './components/Screen2.vue'
import Screen3 from './components/Screen3.vue'

export default {
  name: 'app',
  components: {
    Screen1,
    Screen2,
    Screen3
  }
}
</script>

<style lang="scss">
$mainColor: rgb(255, 198, 26);

html {
  font-family: 'Open Sans', sans-serif;
  font-size: 24px;
  line-height: 1.2;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.separator {
  height: 20px;
  background: linear-gradient(45deg, rgb(0, 0, 0) 25%, rgba(255, 255, 255, 0) 25%) 0 0,
  linear-gradient(45deg, rgba(255, 255, 255, 0) 75%, rgb(0, 0, 0) 75%) 0 0,
  linear-gradient(45deg, rgba(255, 255, 255, 0) 75%, rgb(0, 0, 0) 75%) -10px 10px,
  linear-gradient(45deg, rgb(0, 0, 0) 25%, rgba(255, 255, 255, 0) 25%) 10px -10px;
  background-size: 20px 20px;
  background-color: $mainColor;

  &_small {
    width: 50px;
    margin: 10px auto;
  }
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  margin: auto;
  display: inline-block;
  max-width: 100%;
  max-height: 100%;
  background-color: rgba(0, 0, 0, .7);
}

.close {
  position: absolute;
  z-index: 110;
  top: 5px;
  right: 15px;
  font-weight: 100;

  &:focus {
    outline: none;
  }
}

.color {
  &-white {
    color: #fff;
  }
  &-grey {
    color: #333;
  }
  &-main {
    color: $mainColor;
  }
}

h1, h2, h3, h4, h5, h6 {
  line-height: 1.2;
  font-weight: 800;
}

h1.title {
  font-size: 2.292rem;
  @media (max-width: 575px) {
    font-size: 1.592rem;
  }
}

h2.title {
  font-size: 1.833rem;
  @media (max-width: 575px) {
    font-size: 1.42rem;
  }
}

.subtitle {
  font-size: 1.083rem;
  line-height: 1.385;
  @media (max-width: 575px) {
    font-size: 1rem;
  }
}

.btn {
  background-color: $mainColor;
  border-radius: 0;
  border-color: rgb(0, 0, 0);
  padding: 20px 30px;
  color: rgb(22, 22, 22);
  text-transform: uppercase;
  line-height: 1.2;
  text-align: center;
  @media (max-width: 575px) {
    font-size: 0.5833rem;
  }

  &:hover {
    background-color: darken($mainColor, 9);
  }
}

a {
  color: $mainColor;
  @media (max-width: 575px) {
    font-size: 0.6667rem;
  }

  &:hover {
    text-decoration: none;
    color: darken($mainColor, 9);;
  }
}

/* Slider */
.vueperslides {
  .vueperslides__parallax-wrapper::before,
  .vueperslides__parallax-wrapper::after {
    box-shadow: none;
  }
  .vueperslides__slide {
    padding-left: 80px;
    padding-right: 80px;
    @media (max-width: 575px) {
      padding: 40px 45px 0 60px;
    }
    @media (max-width: 420px) {
      padding: 20px 45px 0 50px;
    }
  }
  .vueperslides__arrow {
    font-size: 2.5em;
    &:focus {
      outline: none;
    }
    @media (max-width: 575px) {
      font-size: 1.5em;
    }
    svg {
      fill: #fff;
    }
  }
}

.slider-item {
  display: flex;

  .slider-info {
    flex-direction: column;
    display: flex;
    justify-content: center;
    @media (max-width: 575px) {
      font-size: .7rem;
    }
    @media (max-width: 420px) {
      font-size: .5rem;
    }

    .slider-title {
      font-size: 1.1rem;
      font-weight: 700;
      @media (max-width: 575px) {
        font-size: .9rem;
      }
      @media (max-width: 420px) {
        font-size: .61rem;
      }
    }
  }

  .slider-img img {
    border-radius: 50%;
    @media (max-width: 575px) {
      width: 90px;
    }
    @media (max-width: 420px) {
      width: 60px;
    }
  }
}

/* /Slider */

/* Form */
.form {
  .btn_submit {
    font-weight: bold;
    text-transform: none;
  }
  .form-check-label {
    color: #fff;
    @media (max-width: 575px) {
      font-size: .7rem;
    }
  }
  input.form-control {
    color: #999;
    background: transparent;
    border-left: none;
    border-right: none;
    border-radius: 0;
    border-color: #999;
    @media (max-width: 575px) {
      font-size: .7rem;
    }

    &:focus {
      box-shadow: none;
      border-color: #fff
    }
  }
}
/* /Form */
</style>
