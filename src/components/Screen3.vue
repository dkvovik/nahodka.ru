<template>
  <b-container fluid class="cost-wrapper">
    <div class="overlay"></div>
    <b-row>
      <b-container>
        <b-row>
          <b-col cols="12" class="mb-3 mb-sm-5">
            <h2 class="title color-white text-center">Стоимость аренды авто <span class="color-main">1600 рублей</span>
              в сутки</h2>
            <p class="subtitle color-white text-center mt-3">Вы сможете оплачивать аренду любым удобным способом</p>
          </b-col>

          <div class="w-100"></div>

          <b-col cols="12" md="4" class="payment text-center mb-3 mb-lg-0" id="connect">
            <img class="payment-icon mb-3" src="../assets/images/uber.png"
                 srcset="../assets/images/uber@2x.png 2x, ../assets/images/uber@3x.png 3x">
            <p class="payment-text text-center color-white">Оплата через баланс Uber</p>
          </b-col>

          <b-col cols="12" md="4" class="payment text-center mb-3 mb-lg-0" id="connect">
            <img class="payment-icon mb-3" src="../assets/images/money.png"
                 srcset="../assets/images/money@2x.png 2x, ../assets/images/money@3x.png 3x">
            <p class="payment-text text-center color-white">Наличный расчет</p>
          </b-col>

          <b-col cols="12" md="4" class="payment text-center mb-3 mb-lg-0" id="connect">
            <img class="payment-icon mb-3" src="../assets/images/card.png"
                 srcset="../assets/images/card@2x.png 2x, ../assets/images/card@3x.png 3x">
            <p class="payment-text text-center color-white">Безналичный расчет</p>
          </b-col>
        </b-row>
      </b-container>
    </b-row>
  </b-container>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.cost-wrapper {
  position: relative;
  padding-top: 125px;
  padding-bottom: 125px;
  background: url(../assets/images/bg-cost.jpg) bottom repeat-x;
  background-size: cover;
  @media (max-width: 574px) {
    padding-top: 75px;
    padding-bottom: 75px;
  }
}

.payment {
  @media (max-width: 767px) {
    display: flex;
    align-items: center;
    padding-left: 40px;
  }
  .payment-icon {
    height: 81px;
    @media (max-width: 767px) {
      margin-right: 25px;
    }
  }
}
</style>