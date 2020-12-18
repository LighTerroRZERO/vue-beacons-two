<template>
  <div class="container">
    <div class="nav">
      <ul class="header_menu">
        <li><a href="#">Home</a></li>
        <li><a href="#">Order services</a></li>
        <li><a href="#">Beacon Marketing</a></li>
      </ul>
    </div>
    <div class="flex-container">
      <div class="discription">

        <h1>DISCOUNT FOR SERVICES</h1>

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
  </div>
</template>

<script>
export default {

};
</script>

<style lang="scss" scoped>
.container {
  .nav{
    .header_menu{
      display: flex;
      justify-content: flex-end;
      li {
        margin-top: 57px;
        a{
          font-family: "Lato Medium";
          font-size: 18px;
          color: #fff;
          text-transform: uppercase;
          padding: 20px 43px;
          margin: 35px 26px 0 0;
          transition: 0.3s ease;
          &:hover{
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
  }
  .flex-container {
    .discription {
      font-family: Lato, sans-serif;
      margin-top: 100px;
      margin-left: auto;
      margin-right: 100px;
      width: 540px;
      color: #fff;
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
  }
}
@media (max-width: 1366px) {
  .header_menu li {
    margin-top: 37px;
  }
  .flex-container {
    .discription{
      margin-top: 0;
      margin-right: 0;
      h3 {
        font-size: 10px;
      }
      p {
        font-size: 5px;
      }
    }
  }
}
</style>
