<template>
  <div>
    <Navthree />
    <NewsHeader title="News Single" />
    <BlogDetails />
    <Footer />
  </div>
</template>

<script>
  import Navthree from "../components/Navthree";
  import NewsHeader from "../components/NewsHeader";
  import Footer from "../components/Footer";
  import BlogDetails from "../components/BlogDetails";
  export default {
    components: {
      BlogDetails,
      Footer,
      NewsHeader,
      Navthree
    },
    head(){
      return {
        title: "Codesk | News Single"
      }
    }
  }
</script>
