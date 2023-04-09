<template>
    <div>
      <section class="footer-area">
        <div class="container">
          <div class="row">
            <div class="col-lg-4 col-md-6 col-sm-8">
              <div class="footer-about mt-30">
                <div class="logo">
                  <a href="/" style="font-weight: bold; color:white; font-size: small; ">Unviersal Evangelical <br/> Church</a>
                </div>
                <p></p>
                <ul>
                  <li><a href="mailto:info@uec.com.ng">info@uec.com.ng</a></li>
                  <li><a href="mailto:universalevangelicalchurch@gmail.com">universalevangelicalchurch@gmail.com</a></li>
                </ul>
              </div>
            </div>
            <div class="col-lg-2 col-md-6 col-sm-6">
              <div class="footer-list mt-30">
                <h4 class="title">Navs</h4>
                <ul>
                  <li><a href="#">About us</a></li>
                  <li><a href="#">Latest events</a></li>
                  <li><a href="#">News & articles</a></li>
                  <li><a href="#">Contact us</a></li>
                </ul>
              </div>
            </div>
            <div class="col-lg-3 col-md-6 col-sm-6">
              <div class="footer-list pl-35 mt-30">
                <h4 class="title">Explore</h4>
                <ul>
                  <li><a href="#">Our history</a></li>
                  <li><a href="#">Help & support</a></li>
                  <li><a href="#">Privacy policy</a></li>
                  <li><a href="#">Terms & condition</a></li>
                </ul>
              </div>
            </div>
            <div class="col-lg-3 col-md-6">
              <div class="footer-address mt-30">
                <h3 class="title">Address</h3>
                <p>Lagos, Nigeria</p>
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3963.4168751443103!2d3.3544876149288765!3d6.594998424157299!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x103b9238d78c85bb%3A0x4879a9d770c059c6!2sUniversal%20Church%20Of%20The%20Kingdom%20Of%20God!5e0!3m2!1sen!2sng!4v1681022204206!5m2!1sen!2sng" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe> 

                <span><i class="fa fa-map-marker"></i> Find us on Map</span>
              </div>
            </div>
          </div>
        </div>
        <div class="footer-copyright-area">
          <div class="container">
            <div class="row">
              <div class="col-lg-12">
                <div class="footer-copyright d-block d-md-flex justify-content-between align-items-center">
                  <p>© Copyright 2023 by Universal Evangelical Church</p>
                  <ul>
                    <li><a href="#"><i class="fa fa-facebook-square"></i></a></li>
                    <li><a href="#"><i class="fa fa-twitter"></i></a></li>
                    <li><a href="#"><i class="fa fa-instagram"></i></a></li>
                    <li><a href="#"><i class="fa fa-dribbble"></i></a></li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="footer-pattern">
          <img src="/assets/images/footer-pattern.png" alt="">
        </div>
        <div class="footer-logo">
          <img src="/assets/images/footer-logo.png" alt="">
        </div>
      </section>

      <div class="go-top-area">
        <div class="go-top-wrap">
          <div class="go-top-btn-wrap">
            <div @click="scrollTop" :class="`go-top go-top-btn ${scrollBtn ? 'active' : ''}`">
              <i class="fa fa-angle-double-up"></i>
              <i class="fa fa-angle-double-up"></i>
            </div>
          </div>
        </div>
      </div>

    </div>
</template>

<script>
  export default {
    name: "Footer",
    data(){
      return {
        scrollBtn: false
      }
    },
    mounted() {
      window.addEventListener('scroll', this.handleScroll);
    },

    methods: {

      handleScroll () {

        if (window.scrollY > 70) {
          this.scrollBtn = true
        }
        else if (window.scrollY < 70) {
          this.scrollBtn = false
        }
      },

      scrollTop () {
        window.scrollTo(0, 0);
      }

    }
  }
</script>

<style scoped>

</style>
