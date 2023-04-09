<template>
  <div>
    <NavThree /> 
    <PageHeader title="Events" />
    <UpcomingEventsTwo />
    <Footer />
  </div>
</template>

<script>
  import NavThree from "../components/NavThree";
  import PageHeader from "../components/PageHeader";
  import Footer from "../components/Footer";
  import UpcomingEventsTwo from "../components/UpcomingEventsTwo";
  import WeListen from "../components/WeListen";
  export default {
    components: {
      WeListen,
      UpcomingEventsTwo,
      Footer,
      PageHeader,
      NavThree
    },
    head(){
      return {
        title: "UEC | Events"
      }
    }
  }
</script>
