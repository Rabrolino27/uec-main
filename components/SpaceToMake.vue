<template>
  <section class="space-to-make-area pt-120 pb-120" id="about">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-6">
          <div class="space-to-make-thumb animated wow fadeInLeft" data-wow-duration="1500ms" data-wow-delay="0ms">
            <img src="/assets/images/about02.avif" alt="">
            <div class="thumb-content">
              <span> Branches <br> worldwide</span>
            </div>
          </div>
        </div>
        <div class="col-lg-6 col-md-10">
          <div class="space-to-make-content">
            <h3 class="title">About Us.</h3>
            <p v-if="data">{{ data }}</p>
            
          </div>
        </div>
      </div>
    </div>
    <div class="shape-pattern">
      <img src="/assets/images/shape-pattern.png" alt="">
    </div>
    <div class="shape-pattern-2">
      <img src="/assets/images/we-know-line.png" alt="">
    </div>
  </section>
</template>

<script>
      import {url} from '../data/api'

    export default {
      data() {
        return {
          data: null,
        };
      },
      methods: {
        async fetchData() {      
          const response = await fetch(`${url}/about`, {
                  method : "GET",
              });
              const res = await response.json();
              this.data = await res.data[0]['about_information'];
              console.log(this.data)
        },    
      },
      name: "SpaceToMake",
        async mounted(){
          this.fetchData();   
    }
    }
    

</script>

<style scoped>

</style>
