<template>
<footer>
  <div class="container">
    <div class="content">
      <div class="support_number">SUPPORT:(844) 295-0900</div>
      <div class="support_mail">support@frontdeskhelpers.com</div>
      <div class="footer-links">
        <div class="social_links">
          <a href="#" class="social"><i class="fb"></i></a>
          <a href="#" class="social"><i class="g"></i></a>
          <a href="#" class="social"><i class="y"></i></a>
          <a href="#" class="social"><i class="in"></i></a>
        </div>

        <div class="links">
          <a href="#">Privacy Policy</a>
          <a href="#">Terms of Service</a>
          <a href="#">Terms of Sales</a>
        </div>
      </div>
      <div class="copyrights">© 2017 FDH CLOUD</div>
    </div>
  </div>
  <div class="img-hand">
    <img src="@/assets/img/wave-vs-hand.png" alt class='absolute-image'>
  </div>
</footer>
</template>

<script>
export default {

};
</script>

<style lang="scss" scoped>

footer {
  background: url("../assets/img/footer-bg.png") no-repeat;
  background-size: cover;
  display: block;
  position: relative;
  float: left;
  width: 100%;
  img {
    position: absolute;
    box-sizing: border-box;
    left: 0;
    bottom: 0;
    height: 170%;
  }
}

.container {
  font-family: Lato, sans-serif;
  font-weight: 400;
  color: #fff;
  text-align: center;
  margin-top: 30px;
}

.content {
  margin-left: -15px;
  margin-right: -15px;
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
}

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
    i {
      font-family: FontAwesome;
    }
    .fb:before {
      content: "\f09a";
    }
    .g:before {
      content: "\f0d5";
    }
    .y:before {
      content: "\f167";
    }
    .in:before {
      content: "\f0e1";
    }
    &:hover {
      background-color: #fff;
      transition: 0.3s;
      i {
        color: #5bd293;
      }
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
</style>
