<template>
  <header class="header">
    <div class="container">
      <div class="menu-button"><span></span></div>
      <div class="nav">
        <ul class="header__menu">
          <li><a href="#">Home</a></li>
          <li><a href="#">Order services</a></li>
          <li><a href="#">Beacon Marketing</a></li>
        </ul>
      </div>
      <div class="content">
        <div class="header__img">
          <img src="@/assets/img/head-abslut.png" alt class='absolute-image'>
        </div>
      </div>
      <div class="content discription">

        <h1>Discount for services</h1>

        <h3>Our advertisement services cost $10 per
          beacon per month, and we offer wholesale discounts:</h3>

        <p>Free installation of the beacons is also an option, but
          then their marketing capabilities will be used by third
          parties also. How to Get Connected To get connected
          to our service or find out more information, please call
          us at (844)-295-0900 or purchase our service through
          our site at https://fdh.cloud/order/services</p>

      </div>
    </div>
  </header>
</template>

<script>
export default {

};
</script>

<style lang="scss" scoped>
.header {
  display: block;
  position: relative;
  width: 100%;
  background: url("../assets/img/head-bg.png") no-repeat;
  background-size: cover;
}

.nav{
  display: block;
  position: relative;
  margin-top: 57px;
}

.menu-button {
  display: none;
}

.header__menu{
  display: block;
  float: right;
  position: relative;
  margin-block-start: 1em;
  margin-block-end: 1em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
  padding-inline-start: 40px;
  box-sizing: border-box;
  li {
    display: inline-block;
    margin-left: 96px;
    a{
      display: block;
      position: relative;
      box-sizing: border-box;
      font-family: "Lato Medium";
      font-size: 18px;
      color: #fff;
      text-transform: uppercase;;
      transition: 0.3s ease;
      outline: none;
      &:hover{
        padding: 15px 30px;
        margin: -15px -30px;
        font-family: "Lato Black";
        background-color: #fff;
        color: #43cb83;
        border-radius: 50px;
        box-shadow: 10px 0 37px rgba(0,0,0,0.5);
        transition: 0.3s ease;
      }
    }
  }
}

.content {
  display: block;
  position: relative;
  box-sizing: border-box;
  min-height: 1px;
  text-align: left;
  padding: 0 15px;
}

.header__img {
  display: block;
  position: absolute;
  width: 100%;
  left: -8%;
  box-sizing: border-box;

  img{
    width: 100%;
    object-fit: cover;
    box-sizing: border-box;
    border-style: none;
    vertical-align: middle;
    border: 0;
  }
}

.discription {
  font-family: Lato, sans-serif;
  margin-top: 78px;
  margin-bottom: 100px;
  color: #fff;

  h1 {
    display: block;
    text-transform: uppercase;
  }
  h3 {
    font-weight: bold;
    font-size: 24px;
    line-height: 37px;
    margin-top: 60px;
  }
  p {
    font-weight: 400;
    font-size: 18px;
    line-height: 30px;
    margin-top: 40px;
  }
}

@media screen and (max-width: 1366px) {
  .header__img {
    left: 0;
  }
}

@media (min-width: 1030px) {
  .content {
    width: 50%;
    float: left;
  }
  .nav {
    width: 100%;
    float: left;
  }
}

@media (max-width: 1030px) {
  .header__img {
    display: none;
  }
  .header__menu li{
    margin-left: 70px;
  }
}

@media screen and (max-width: 690px){
  .menu-button {
    display: block;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background-color: #fff;
    box-shadow: 10px 0 37px rgba(0,0,0,0.5);
    position: relative;
    left: 15px;
    top: 20px;
    z-index: 4;
    box-sizing: border-box;
    cursor: pointer;

    span {
      display: block;
      height: 2px;
      width: 18px;
      background-color: #000;
      position: absolute;
      left: 50%;
      top: 50%;
      margin-left: -9px;
      margin-top: -1px;
    }

    span::before {
      display: block;
      height: 2px;
      width: 18px;
      background-color: #000;
      position: absolute;
      left: 50%;
      top: 50%;
      margin-left: -9px;
      margin-top: -6px;
      content: '';
    }
    span::after {
      display: block;
      height: 2px;
      width: 18px;
      background-color: #000;
      position: absolute;
      left: 50%;
      top: 50%;
      margin-left: -9px;
      margin-top: 4px;
      content: '';
    }
  }

  .nav {
    display: none;
  }
}
</style>
