<template>
  <section class="upcoming-events-area events-page">
    <div class="container">
      <div class="row">
        <div class="col-lg-12">
          <div class="upcoming-events-item">
            <div class="item mt-20" v-for="item in data">
              <div class="row align-items-center">
                <div class="col-lg-9">
                  <div class="upcoming-events-content d-block d-md-flex align-items-center">
                    <div class="thumb">
                      <img  :src="`${img}/uploads/${item.image}`" style="width:130px; height:128px;" alt="">
                      <div class="date">
                        <span>{{formatDay(item.date)}} <br> {{formatMonth(item.date)}}</span>
                      </div>
                    </div>
                    <div class="content ml-65">
                      <ul>
                        <li><i class="fa fa-clock-o"></i> {{formatTime(item.date)}} </li>
                        <li><i class="fa fa-user-o"></i> Admin </li>
                      </ul>
                      <h4 class="title">{{item.name}}</h4>
                      <p>{{item.details}}</p>
                    </div>
                  </div>
                </div>
                <div class="col-lg-3">
                  <div class="events-btn text-left text-lg-right">
                    <!-- <a class="main-btn main-btn-2" href="single-news.html">Join event</a> -->
                  </div>
                </div>
              </div>
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
        name: "UpcomingEventsTwo",
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
          return `${day}/${month}`
        },
        formatTime(timestamp) {
          const date = new Date(timestamp)
          const month = date.toLocaleString('default', { month: 'short' })
          const year = date.getFullYear()
          const hours = date.getHours()
          const minutes = date.getMinutes()
          return `${hours.toString().padStart(2, '0')}:${minutes.toString().padStart(2, '0')}`
        },
        formatDay(timestamp) {
          const date = new Date(timestamp)
          const month = date.toLocaleString('default', { month: 'short' })
          const year = date.getFullYear()
          const hours = date.getHours()
          const minutes = date.getMinutes()
          const day = date.getDate()
          return `${day}`
        },
        formatMonth(timestamp) {
          const date = new Date(timestamp)
          const month = date.toLocaleString('default', { month: 'short' })
          const year = date.getFullYear()
          const hours = date.getHours()
          const minutes = date.getMinutes()
          return `${month}`
        },
        async fetchData() {      
          const response = await fetch(`${url}/events`, {
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
