<template>
  <b-container fluid class="provide-wrapper">
    <b-row>
      <b-container>
        <b-row>
          <b-col cols="12">
            <h2 class="title color-grey text-center mb-3 mb-sm-5">Мы предоставим</h2>
          </b-col>
          <div class="w-100 mb-4"></div>
          <b-col cols="12" sm="6" md="3" class="provide text-center mb-3 mb-md-0">
            <img class="provide-icon mb-3" src="../assets/images/car.png"
                 srcset="../assets/images/car@2x.png 2x, ../assets/images/car@3x.png 3x">
            <p class="provide-text text-center color-grey">Автопарк из разных марок машин не старше 2-х лет</p>
          </b-col>
          <b-col cols="12" sm="6" md="3" class="provide text-center mb-3 mb-md-0">
            <img class="provide-icon mb-3" src="../assets/images/taxi.png"
                 srcset="../assets/images/taxi@2x.png 2x, ../assets/images/taxi@3x.png 3x">
            <p class="provide-text text-center color-grey">Подключение к Я.Такси и Uber</p>
          </b-col>
          <b-col cols="12" sm="6" md="3" class="provide text-center mb-3 mb-sm-0">
            <img class="provide-icon mb-3" src="../assets/images/tech.png"
                 srcset="../assets/images/tech@2x.png 2x, ../assets/images/tech@3x.png 3x">
            <p class="provide-text color-grey">Техническое обслуживание</p>
          </b-col>
          <b-col cols="12" sm="6" md="3" class="provide text-center">
            <img class="provide-icon mb-3" src="../assets/images/doc.png"
                 srcset="../assets/images/doc@2x.png 2x, ../assets/images/doc@3x.png 3x">
            <p class="provide-text text-center color-grey">Договор</p>
          </b-col>
        </b-row>
      </b-container>
    </b-row>
  </b-container>
</template>

<script>
export default {}
</script>

<style scoped lang="scss">
.provide-wrapper {
  padding-top: 125px;
  padding-bottom: 125px;
  background: url(../assets/images/bg-provide.png?8d7a1dd…) bottom repeat-x;
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
</style>