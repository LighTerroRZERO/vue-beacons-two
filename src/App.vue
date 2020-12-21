<template>
  <div id="app">
    <Header/>

    <CardsContainer/>

    <SectionForm/>

    <Footer/>
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

h1 {
  font-family: "Lato Black";
  font-size: 36px;
  margin: 0.67em 0;
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
  margin-right: auto;
  margin-left: auto;
  padding: 0 30px;
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

@media (min-width: 1366px) {
  .container {
    width: 1170px;
  }
}

@media (max-width: 1366px) and (min-width: 1030px) {
  .container {
    width: 970px;

  }
}

@media (max-width: 1030px) and (min-width: 810px) {
  .container {
    width: 750px;
  }
}
</style>
