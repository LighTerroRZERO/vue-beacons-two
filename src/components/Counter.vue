<template>
  <div class="counter">
    <span class="sign" v-on:click="counterDown()">-</span>
    <span>{{ quantity }}</span>
    <span class="sign" v-on:click="counterUp()">+</span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      quantity: 1,
      counterUp() {
        if (this.quantity < 999) {
          // eslint-disable-next-line no-plusplus
          this.quantity++;
        }
      },
      counterDown() {
        if (this.quantity > 1) {
          // eslint-disable-next-line no-plusplus
          this.quantity--;
        }
      },
    };
  },
};
</script>

<style lang="scss" scoped>
.counter {
  position: relative;
    width: 100px;
    height: 30px;
    text-align: center;
    border-radius: 10px;
    border: 1px solid #e6e6e6;
    margin: 0 auto;
    display: flex;
    justify-content: center;
    align-items: center;
    line-height: 25px;

  .sign {
    font-family: Lato, sans-serif;
    cursor: pointer;
    padding: 0 5px;
    font-size: 17px;
    font-weight: 700;
    color: #282828;
    &:hover {
      cursor: pointer;
    }
  }

  span {
    border: none;
    text-align: center;
    width: 50px;
  }
}
</style>
