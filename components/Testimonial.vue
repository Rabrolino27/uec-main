<template>
  <div>
    <div class="testimonial-title-area">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="testimonial-title text-center">
              <h2 class="title">Testimonies.</h2>
            </div>
          </div>
        </div>
      </div>
    </div>
    <section class="testimonial-area">
      <div class="container">
        <div class="row testimonial-active">
          <swiper :options="swiperOptions">
              <swiper-slide v-for="item in data">
                    <div class="testimonial-item text-center">
                      <p>{{ item.details }}</p>
                      <h4 class="title">{{ item.name }}</h4>
                      <span>Christain</span>
                      <img :src="`${img}/uploads/${item.image}`" alt="testimonial" style="height: 80px; width: 80px;">
                    
                    </div>
              </swiper-slide>          
          </swiper>
        </div>
      </div>
      <div class="testimonial-pattern">
        <img src="assets/images/testimonial-pattern.png" alt="">
      </div>
    </section>
  </div>
</template>

<script>
  import { Swiper, SwiperSlide, directive } from 'vue-awesome-swiper';
  import 'swiper/css/swiper.css';
  import {url} from '../data/api';
  import {img} from '../data/api'




  export default {
    name: "Testimonial",
    components: {
      Swiper,
      SwiperSlide
    },
    directives: {
      swiper: directive
    },
    data() {
      return {
        swiperOptions: {
          slidesPerView : 3,
          loop: true,
          speed: 1000,
          spaceBetween : 30,
          autoplay: {
            delay: 3000,
            disableOnInteraction: false
          },
          pagination: {
            el: '.swiper-pagination',
            type: 'bullets',
            clickable: true
          },
          // Responsive breakpoints
          breakpoints: {
            1024:{
              slidesPerView : 3
            },
            768:{
              slidesPerView : 2
            },
            640:{
              slidesPerView : 1
            },
            320:{
              slidesPerView : 1
            }
          }
        },
        data: null,
        img: img
      }
    },
    methods: {
        async fetchData() {      
          const response = await fetch(`${url}/testimony`, {
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
