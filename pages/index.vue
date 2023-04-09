<template>
  <div>
    <NavThree />
    <Slider />
    <SpaceToMake />
    
    <Gallery />
   
    <Testimonial />
    <CallToAction />
    <Blog />
    <Footer />
  </div>
</template>

<script>
  import NavThree from "../components/NavThree";
  import Nav from "../components/Nav";
  import Slider from "../components/Slider";
  import BestCreative from "../components/BestCreative";
  import SpaceToMake from "../components/SpaceToMake";
  import Trusted from "../components/Trusted";
  import Services from "../components/Services";
  import Gallery from "../components/Gallery";
  import Funfacts from "../components/Funfacts";
  import WeKnows from "../components/WeKnows";
  import ChangingArea from "../components/ChangingArea";
  import Testimonial from "../components/Testimonial";
  import CallToAction from "../components/CallToAction";
  import Blog from "../components/Blog";
  import CompanyLogo from "../components/CompanyLogo";
  import Footer from "../components/Footer";

  export default {
    components: {
      Footer,
      CompanyLogo,
      Blog,
      CallToAction,
      Testimonial,
      ChangingArea,
      WeKnows,
      Funfacts,
      Gallery,
      Services,
      Trusted,
      SpaceToMake,
      BestCreative,
      Slider,
      NavThree

    }
  }
</script>
