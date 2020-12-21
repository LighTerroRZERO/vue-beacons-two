<template>
  <section class="form">
    <div class="formImg">
        <img src="@/assets/img/beacons.png" alt class='absolute-image'>
    </div>

    <div class="container">
      <div class="content">
        <h2>A couple of steps to make your store popular</h2>

        <div class="steps-for-form">
          <div class="step" v-bind:class="{ active: stepFirst}">Step 1</div>
          <div class="step" v-bind:class="{ active: stepSecond}">Step 2</div>
          <div class="step" v-bind:class="{ active: stepThird}">Step 3</div>
        </div>

        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
          enim ad minim veniam, quis nostrud exercitation ullamco laboris
          nisi ut aliquip ex ea commodo consequat. Duis aute irure</p>

        <form v-bind:class="{ active: stepFirst}" onsubmit="event.preventDefault();">
          <FormInput
          v-for="input in inputs" :key="input.id" :item="input" @validateInfo="validateInfo" />
          <button @click="nextStep()">Next</button>
        </form>

        <form v-bind:class="{ active: stepSecond}" onsubmit="event.preventDefault();">
          <FormInput
          v-for="input in inputs" :key="input.id" :item="input" @validateInfo="validateInfo" />
          <button @click="nextStep()">Next</button>
        </form>

        <form v-bind:class="{ active: stepThird}">
          <FormInput
          v-for="input in inputs" :key="input.id" :item="input" @validateInfo="validateInfo" />
          <button @click="nextStep()">Next</button>
        </form>
      </div>
    </div>
  </section>
</template>

<script>
import FormInput from './FormInput.vue';

export default {
  components: {
    FormInput,
  },
  data() {
    return {
      inputs: [
        {
          id: 1, type: 'text', name: 'firstName', placeholder: 'Enter First Name',
        },
        {
          id: 2, type: 'text', name: 'lastName', placeholder: 'Enter Last Name',
        },
        {
          id: 3, type: 'email', name: 'email', placeholder: 'Enter Email',
        },
      ],
      step: 1,
      stepFirst: true,
      stepSecond: false,
      stepThird: false,
      isTrueCounter: 0,
    };
  },
  methods: {
    nextStep() {
      if (this.isTrueCounter === 3) {
        this.step += 1;
        switch (this.step) {
          case 1:
            this.stepFirst = true;
            this.stepSecond = false;
            this.stepThird = false;
            break;
          case 2:
            this.stepFirst = false;
            this.stepSecond = true;
            this.stepThird = false;
            break;
          case 3:
            this.stepFirst = false;
            this.stepSecond = false;
            this.stepThird = true;
            break;
          default:
            this.step = 1;
            this.stepFirst = true;
            this.stepSecond = false;
            this.stepThird = false;
            break;
        }
        this.isTrueCounter = 0;
      }
    },
    validateInfo(isTrue) {
      if (isTrue) {
        this.isTrueCounter += 1;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
.form {
  background: url("../assets/img/bg-beacons.png") no-repeat;
  background-size: cover;
  display: block;
  position: relative;
  float: left;
  width: 100%;
  box-sizing: border-box;
  .formImg {
    position: absolute;
    right: 0;
    height: 100%;
    top: 0;

    img{
      object-fit: cover;
      width: 100%;
      height: 100%;
      vertical-align: middle;
      border: 0;
      border-style: none;
    }
  }
}

  .content {
    text-align: center;

    &::before{
      content: ' ';
      display: table;
      box-sizing: border-box;
    }
    &::after{
      clear: both;
      content: ' ';
      display: table;
      box-sizing: border-box;
    }

    h2 {
      margin-top: 60px;
      font-family: Lato, sans-serif;
      font-weight: 700;
      font-size: 36px;
    }
    .steps-for-form {
      display: flex;
      justify-content: center;
      margin-top: 48px;
      margin-bottom: 40px;
      .step {
        font-family: "Lato Black";
        font-size: 22px;
        padding: 15px 34px;
        margin: 0 40px 0;
      }
      .active {
        box-shadow: 15px 0 29px rgba(60, 171, 112, 0.63);
        border-radius: 30px;
        background-color: #fff;
      }
    }
    p {
      font-family: Lato, sans-serif;
      font-weight: 700;
      font-size: 24px;
      text-align: left;
      width: 100%;
      max-width: 800px;
      margin: auto;
      margin-bottom: 31px;
    }
  }
  form {
    margin: 0 300px;
    display: none;
    button {
      display: block;
      margin: 11px auto 50px;
      border-radius: 30px;
      width: 200px;
      height: 55px;
      outline: none;
      background: #fff;
      color: #43cb83;
      font-family: Lato, sans-serif;
      font-size: 27px;
      font-weight: 700;
      text-transform: uppercase;
      border: none;
      transition: 0.3s ease;
      &:hover {
        transition: 0.3s ease;
        transform: scale(1.1);
        box-shadow: 15px 0 29px rgba(60, 171, 112, 0.63);
      }
    }
  }

form.active {
  display: block;
}

</style>
