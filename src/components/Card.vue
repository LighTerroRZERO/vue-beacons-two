<template>
  <div class="card">
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
      <button class="buy-button">Buy now</button>
    </div>
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
.card {
  display: block;
  box-sizing: border-box;
  width: 25%;
  float: left;
  position: relative;
  min-height: 1px;
  padding-left: 15px;
  padding-right: 15px;
}

.beacon-card {
  width: 100%;
  margin-bottom: 40px;
  background-color: #fff;
  text-align: center;
  border: 1px solid #e3e3e3;
  transition: 0.3s ease;
  .card-title {
    font-family: "Lato Medium";
    font-size: 18px;
    text-transform: uppercase;
    margin-top: 15px;
    margin-bottom: 15px;
    padding: 0 20px;
    height: 50px;
  }
  .img-container{
    width: 150px;
    height: 140px;
    margin: 0 auto;
    .image-product {
      width: 100%;
      vertical-align: middle;
      border: 0;
      border-style: none;
    }
  }
  .card-price {
    font-family: Montserrat, sans-serif;
    font-weight: 900;
    font-size: 29px;
    color: #515461;
    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
  }
  .card-info {
    padding: 0 15px;
    font-family: Lato, sans-serif;
    font-weight: 400;
    font-size: 14px;
    line-height: 20px;
    margin-top: 15px;
    height: 150px;
    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
  }
  .card-counter {
    display: block;
    position: relative;
    width: 140px;
    margin: 0 auto;
    span {
      position: absolute;
      top: 4px;
      right: -8px;
      font-size: 12px;
    }
  }
  .buy-button {
    font-family: Lato, sans-serif;
    font-weight: 700;
    font-size: 16px;
    color: #2c2c2c;
    width: 200px;
    height: 40px;
    border: 3px solid #5bd293;
    text-transform: uppercase;
    outline: none;
    background: transparent;
    border-radius: 30px;
    display: block;
    margin: 20px auto;
    transition: 0.5s ease;
  }
  &:hover{
    box-shadow: 8px 0 57px rgba(0, 0, 0, 0.3);
    transition: 0.5s ease;
    transform: scale(1.05);
    .buy-button {
      font-family: "Lato Black";
      font-size: 18px;
      color: #282828;
      background-color: #5bd293;
    }
  }
}
</style>
