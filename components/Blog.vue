<template>
  <section class="news-area pb-150">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-5">
          <div class="news-title text-center">
            <h3 class="title">News & articles.</h3>
          </div>
        </div>
      </div>
      <div class="row justify-content-center">
        <div class="col-lg-4 col-md-7" v-for="item in data">
          <div class="mt-30">
            <div class="news-item bg_cover" style="background-color: gray;">
              <div class="item">
                <img :src="`${img}/uploads/${item.main_image}`" style="width: 100px; height: 100px; margin-bottom: 10px; left: 2px;" alt="">
                <ul>
                  <!-- <li><i class="fa fa-user-o"></i> by admin</li> -->
                  <li style="margin-left: 10px;"><i class="fa fa-date"></i> {{formatDate(item.created_at)}}</li>
                </ul>
              </div>
              <h3 class="title">{{item.title}}</h3>
              <nuxt-link :to="{ path: '/single-news', query: { id: item.id } }"><i class="flaticon-right-arrow"></i></nuxt-link>
            </div>
          </div>
        </div>
       
      </div>
    </div>
    <div class="shape-pattern">
      <img src="/assets/images/shape-pattern.png" alt="">
    </div>
  </section>
</template>

<script>
 import {url} from '../data/api';
 import {img} from '../data/api'

    export default {
        name: "Blog",
        data() {
          return {
            data: null,
            img:img
          };
      },
      methods: {
        formatDate(timestamp) {
          const date = new Date(timestamp)
          const month = date.toLocaleString('default', { month: 'short' })
          const year = date.getFullYear()
          return `${month}/${year}`
        },
        async fetchData() {      
          const response = await fetch(`${url}/blogs/home`, {
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
