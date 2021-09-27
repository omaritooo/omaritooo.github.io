<template>
  <div id="app">
    <Navbar></Navbar>
    <Header></Header>
    <SectionOne></SectionOne>
    <SectionTwo></SectionTwo>
    <SectionThree></SectionThree>
    <SectionFour></SectionFour>
    <Footer></Footer>
  </div>
</template>

<script>
// import Header from "./components/Header.vue";
// import SectionOne from "./components/Section1.vue";
// import SectionTwo from "./components/Section2.vue";
import Navbar from "./components/Navbar.vue";
import Header from "./components/Header.vue";
import SectionOne from "./components/Section1.vue";
import SectionTwo from "./components/Section2.vue";
import SectionThree from "./components/Section3.vue";
import SectionFour from "./components/Section4.vue";
import Footer from "./components/Footer.vue";

// import SectionThree from "./components/Section3.vue";
export default {
  name: "App",
  data() {
    return {
      isDark: true,
    };
  },
  components: {
    Navbar,
    Header,
    SectionOne,
    SectionTwo,
    SectionThree,
    SectionFour,
    Footer,
  },
};
</script>

<style>
.app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
