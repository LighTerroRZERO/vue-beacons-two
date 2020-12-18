<template>
  <div id="app">
    <header>
      <Header/>
      <img src="@/assets/img/head-abslut.png" alt class='absolute-image'>
    </header>

    <section class="beacons">
      <div class="container">
        <h1>Choose beacons and fill in the order form?</h1>
        <CardsContainer/>
      </div>
    </section>

    <section class="form">
      <SectionForm/>
      <div class="formImg">
        <img src="@/assets/img/beacons.png" alt class='absolute-image'>
      </div>
    </section>

    <footer>
      <img src="@/assets/img/wave-vs-hand.png" alt class='absolute-image'>
      <Footer/>
    </footer>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import CardsContainer from './components/CardsCotainer.vue';
import SectionForm from './components/SectionForm.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'app',
  components: {
    Header,
    CardsContainer,
    SectionForm,
    Footer,
  },
  data() {
    return {
    };
  },
};
</script>

<style lang="scss">
@import "./components/reset.scss";
@import "./components/fonts.scss";

header {
  background: url("./assets/img/head-bg.png") no-repeat;
  background-size: 100%;
  display: block;
  position: relative;
  width: 100%;
  min-height: 700px;
  img{
    position: absolute;
    box-sizing: border-box;
    top: 0;
    left: 0;
    height: 110%;
    margin-top: 5%;
  }
}

.beacons{
  margin: 75px 0 40px;
  color: #282828;
  h1 {
    text-align: center;
    margin-bottom: 64px;
  }
  .cards {
    display: flex;
  }
}

.form {
  background: url("./assets/img/bg-beacons.png") no-repeat;
  background-size: cover;
  display: block;
  position: relative;
  float: left;
  width: 100%;
  .formImg {
    position: absolute;
    box-sizing: border-box;
    right: 0;
    height: 100%;
    top: 0;
    margin-top: -23px;
  }
}

footer {
  background: url("./assets/img/footer-bg.png") no-repeat;
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

h1 {
  font-family: "Lato Black";
  font-size: 36px;
}

li {
  list-style-type: none;
}

a {
  text-decoration: none;
  &:visited{
    color: #fff;
  }
}

.container{
  display: block;
  width: 1170px;
  margin: auto;
}

@media (max-width: 1366px) {
  header img {
    height: 50%;
  }
  footer img {
    height: 100%
  }
  .container {
    max-width: 960px;
  }
  h1 {
    font-size: 30px;
  }
}

@media (max-width: 1200px) {
  .absolute-image {
    display: none;
  }
}
</style>
