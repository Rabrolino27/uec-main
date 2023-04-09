<template>
  <div>
    <Navthree />
    <NewsHeader title="News" />
    <BlogPage />
    <Footer />
  </div>
</template>

<script>
  import Navthree from "../components/Navthree";
  import NewsHeader from "../components/NewsHeader";
  import Footer from "../components/Footer";
  import BlogPage from "../components/BlogPage";
  import {url} from '../data/api';
  import {img} from '../data/api'
  export default {
  data () {
    return {
      img:img,
      data: null
    }
  },
  methods: {
        formatDate(timestamp) {
          const date = new Date(timestamp)
          const month = date.toLocaleString('default', { month: 'short' })
          const year = date.getFullYear()
          return `${month}/${year}`
        },
        async fetchData() {      
          const response = await fetch(`${url}/blogs`, {
                  method : "GET",
              });
              const res = await response.json();
              this.data = await res.data;
              console.log(this.data)
        },    
      },
    components: {
      BlogPage,
      Footer,
      NewsHeader,
      Navthree
    },
    head(){
      return {
        title: "UEC | News"
      }
    }
  }
</script>
