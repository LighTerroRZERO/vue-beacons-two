<template>
  <div class="beacon-card">
    <h2 class="card-title">{{ item.title }}</h2>
    <div class="img-container">
      <img :src=item.image alt class="image-product">
    </div>
    <h3 class="card-price">${{ item.price }}</h3>
    <p class="card-info">{{ item.info }}</p>
    <div class="card-counter">
      <Counter/>
      <span>шт</span>
    </div>
    <button class="buy-product">Buy now</button>
  </div>
</template>

<script>
import Counter from './Counter.vue';

export default {
  components: {
    Counter,
  },
  props: {
    item: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {

    };
  },
};
</script>

<style lang="scss" scoped>
.beacon-card {
  background-color: #fff;
  flex-basis: 25%;
  text-align: center;
  border: 1px solid #e3e3e3;
  margin-right: 10px;
  transition: 0.3s ease;
  .card-title {
    height:48px;
    margin: 15px 0;
    padding: 0 15px;
    font-family: "Lato Medium";
    font-size: 24px;
    text-transform: uppercase;
  }
  .img-container{
    width: 150px;
    height: 150px;
    margin: auto;
    .image-product {
      width: 100%
    }
  }
  .card-price {
    font-family: Montserrat, sans-serif;
    font-size: 29px;
    color: #515461;
    margin-top: 15px;
  }
  .card-info {
    height: 130px;
    margin: 15px 0;
    padding: 0 15px;
    font-family: Lato, sans-serif;
    font-weight: 400;
    font-size: 16px;
    line-height: 20px;
    margin-bottom: 35px;
  }
  .card-counter {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 21px;
    span {
      margin-left: 10px;
    }
  }
  .buy-product {
    font-family: Lato, sans-serif;
    font-weight: 700;
    font-size: 16px;
    color: #2c2c2c;
    width: 200px;
    height: 40px;
    border: 4px solid #5bd293;
    border-radius: 28px;
    text-transform: uppercase;
    margin: 0 42px 29px;
    outline: none;
  }
  &:hover{
    box-shadow: 8px 0 57px rgba(0, 0, 0, 0.3);
    transition: 0.5s ease;
    transform: scale(1.05);
    .buy-product {
      font-family: "Lato Black";
      font-size: 18px;
      color: #282828;
      background-color: #5bd293;
    }
  }
}
@media (max-width: 1366px) {
  .beacon-card {
    margin-bottom: 10px;
    .card-title {
      font-size: 20px;
    }
    .card-info {
      line-height: 15px;
    }
    .buy-product {
      font-size: 14px;
  }
    &:hover {
      .buy-product{
        font-size: 16px;
      }
    }
  }
}
</style>
