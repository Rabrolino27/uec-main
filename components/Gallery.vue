<template>
  <section class="gallery-area">
    <div class="container">
      <div class="row">
        <div class="col-lg-12">
          <div class="gallery-title text-center">
            <h3 class="title">Our photo gallery</h3>
          </div>
        </div>
      </div>
    </div>
    <div class="container-fluid p-0">
      <div class="gallery-itmes">
        <div class="row no-gutters gallery-active">
            <div class="col-lg-3">
            <div class="gallery-thumb">
              <img src="/assets/images/gallery1.jpeg" alt="gallery" style="height: 300px;">
              <a class="main-btn image-popup galleryOne" href="/assets/images/gallery1.jpeg"><i class="flaticon-plus"></i></a>
            </div>
          </div>
          <div class="col-lg-3">
            <div class="gallery-thumb">
              <img src="/assets/images/gallery2.jpeg" alt="gallery" style="height: 300px;">
              <a class="main-btn image-popup galleryOne" href="/assets/images/gallery2.jpeg"><i class="flaticon-plus "></i></a>
            </div>
          </div>
          <div class="col-lg-3">
            <div class="gallery-thumb">
              <img src="/assets/images/gallery3.jpeg" alt="gallery" style="height: 300px;">
              <a class="main-btn image-popup galleryOne" href="/assets/images/gallery3.jpeg"><i class="flaticon-plus"></i></a>
            </div>
          </div>
          <div class="col-lg-3">
            <div class="gallery-thumb">
              <img src="/assets/images/gallery4.jpeg" alt="gallery" style="height: 300px;">
              <a class="main-btn image-popup galleryOne" href="/assets/images/gallery4.jpeg"><i class="flaticon-plus"></i></a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>


<script>
  export default {
  name: "Gallery",
  mounted() {
    new GLightbox({
      selector: '.galleryOne',
      touchNavigation: true,
      loop: true,
      autoplayVideos: true
    });
  }

  }
</script>
<style scoped>

</style>
