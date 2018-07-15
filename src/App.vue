<template>
  <div id="app">
    <screen1></screen1>
    <div class="separator"></div>
    <screen2></screen2>
  </div>
</template>

<script>
import Screen1 from './components/Screen1.vue'
import Screen2 from './components/Screen2.vue'

export default {
  name: 'app',
  components: {
    Screen1,
    Screen2
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
}

.color-white {
  color: #fff;
}
.color-grey {
  color: #333;
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
</style>
