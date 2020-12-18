<template>
<div class="container">
  <div class="support_number">SUPPORT:(844) 295-0900</div>
  <div class="support_mail">support@frontdeskhelpers.com</div>
  <div class="footer-links">
    <div class="social_links">
      <a href="#" class="social"><i></i></a>
      <a href="#" class="social"><span></span></a>
      <a href="#" class="social"><span></span></a>
      <a href="#" class="social"><span></span></a>
    </div>

    <div class="links">
      <a href="#">Privacy Policy</a>
      <a href="#">Terms of Service</a>
      <a href="#">Terms of Sales</a>
    </div>
  </div>
  <div class="copyrights">© 2017 FDH CLOUD</div>
</div>
</template>

<script>
export default {

};
</script>

<style lang="scss" scoped>
.container {
  font-family: Lato, sans-serif;
  font-weight: 400;
  color: #fff;
  text-align: center;
  margin-top: 30px;
  .support_number {
    font-size: 24px;
    margin-bottom: 15px;
  }
  .support_mail {
    font-size: 22px;
    margin-bottom: 38px;
  }
  .social_links {
    .social {
      display: inline-block;
      height: 57px;
      width: 57px;
      border-radius: 50%;
      border: 1px solid #fff;
      background: transparent;
      margin: 0 20px;
      line-height: 56px;
      color: #fff;
      font-size: 26px;
      transition: 0.3s;
      &:hover {
        background-color: #fff;
        transition: 0.3s;
      }
    }
  }
  .links {
    margin: 45px auto 36px;
    font-size: 20px;
    a {
      margin: auto 22px;
    }
  }
  .copyrights {
    margin-bottom: 45px;
    font-size: 16px;
  }
}
</style>
