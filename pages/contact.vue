<template>
  <div>
    <Navthree />
    <ContactHeader title="Contact" />
    <ContactInfo />
    <WriteMessageThree />
    <GMap />
    <Footer />
  </div>
</template>

<script>
  import Navthree from "../components/Navthree";
  import ContactHeader from "../components/ContactHeader";
  import Footer from "../components/Footer";
  import ContactInfo from "../components/ContactInfo";
  import WriteMessageThree from "../components/WriteMessageThree";
  import GMap from "../components/GMap";
  export default {
    components: {
      GMap,
      WriteMessageThree,
      ContactInfo,
      Footer,
      ContactHeader,
      Navthree
    },
    head(){
      return {
        title: "UEC | Contact"
      }
    }
  }
</script>
