<template>
  <section class="news-2-area news-page">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-4 col-md-7 col-sm-9" v-for="item in data">
          <div class="news-item mt-30">
            <div class="news-thumb">
              <img :src="`${img}/uploads/${item.main_image}`" style="width: 370px; height: 316px;" alt="">
            </div>
            <div class="news-content">
              <ul>
                <li><i class="fa fa-user-o"></i> by admin</li>
                <!-- <li><i class="fa fa-comments-o"></i> 2 comments</li> -->
              </ul>
              <h3 class="title">{{item.title}}</h3>
              <nuxt-link :to="{ path: '/single-news', query: { id: item.id } }"><i class="flaticon-right-arrow"></i></nuxt-link>
            </div>
          </div>
        </div>
       
      </div>
    </div>
  </section>
</template>

<script>
  import {url} from '../data/api';
  import {img} from '../data/api'
    export default {
        name: "BlogPage",
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
      async mounted(){
          this.fetchData();   
    }
    }
</script>

<style scoped>

</style>
