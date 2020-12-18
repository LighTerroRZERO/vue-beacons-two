<template>
  <div class="counter">
    <span v-on:click="counterDown()">-</span>
    <span>{{ quantity }}</span>
    <span v-on:click="counterUp()">+</span>
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
  width: 100px;
  border: 1px solid #e3e3e3;
  border-radius: 25px;
  display: flex;
  justify-content: space-around;
  align-items: center;
  span {
    font-family: Lato, sans-serif;
    font-weight: 400;
    font-size: 20px;
    &:hover {
      cursor: pointer;
    }
  }
}
</style>
