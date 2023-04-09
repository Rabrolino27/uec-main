<template>
  <section class="blog-details">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-8">
          <div class="blog-details__main" v-if="data">
            <div class="blog-details__image">
              <img :src="`${img}/uploads/${data.main_image}`"  alt="thumb" style="width: 770px; height: 464px;">
            </div><!-- /.blog-details__image -->
            <div class="blog-details__content">
              <div class="blog-one__meta">
                <a href="#"><i class="fa fa-user-o"></i> by admin</a>
                <!-- <a href="#"><i class="fa fa-comments-o"></i> 2 comments</a> -->
              </div><!-- /.blog-one__meta -->
              <h3>{{data.title}}</h3>
              <p>{{data.paragraph_one}}</p>
              <p>{{data.paragraph_two}}</p>
              <img v-if="data.mid_image"   :src="`${img}/uploads/${data.mid_image}`" style="width:300; height:464;" alt="thumb">
              <p>{{data.paragraph_three}}</p>
              <img v-if="data.closing_image"  :src="`${img}/uploads/${data.closing_image}`" style="width:300; height:464;" alt="thumb">

              <p>{{data.paragraph_four}}</p>
            </div><!-- /.blog-details__content -->
            <div class="blog-details__meta">
              <div class="blog-details__tags">
                <span>Tags: </span> <a href="#">Christainity</a> <a href="#"></a> <a href="#"></a>
              </div><!-- /.blog-details__tags -->
              <div class="blog-details__share">
                <ul>
                  <li><a href="#"><i class="fa fa-facebook-square"></i></a></li>
                  <li><a href="#"><i class="fa fa-twitter"></i></a></li>
                  <li><a href="#"><i class="fa fa-instagram"></i></a></li>
                  <li><a href="#"><i class="fa fa-pinterest-p"></i></a></li>
                </ul>
              </div><!-- /.blog-details__share -->
            </div><!-- /.blog-details__meta -->
          </div><!-- /.blog-details__main -->

         <!-- /.blog-author -->

  <!--    <div class="comment-one">
            <h3 class="comment-one__block-title">2 Comments</h3>/.comment-one__block-title -->
      <!--       <div class="comment-one__single">
              <div class="comment-one__image">
                <img src="/assets/images/comment-1-1.jpg" alt="">
              </div> /.comment-one__image -->
        <!--       <div class="comment-one__content">
                <h3>Kevin Martin <span class="comment-one__date">20 April, 2020</span></h3>

                <p>Lorem Ipsum has industr standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. </p>
              </div> /.comment-one__content -->
           <!--    <div class="blog-btn">
                <a href="#" class="main-btn main-btn-2">Reply <i class="flaticon-right-arrow"></i></a>
              </div>
              
            </div>
            <div class="comment-one__single">
              <div class="comment-one__image">
                <img src="/assets/images/comment-1-2.jpg" alt="">
              </div> /.comment-one__image -->
         <!--      <div class="comment-one__content">
                <h3>Sarah albert <span class="comment-one__date">20 April, 2020</span></h3>
                <p>Lorem Ipsum has industr standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. </p>
              </div> /.comment-one__content -->
       <!--        <div class="blog-btn">
                <a href="#" class="main-btn main-btn-2">Reply <i class="flaticon-right-arrow"></i></a>
              </div>
              /.thm-btn comment-one__btn -->
          <!--   </div> /.comment-one__single -->
       <!--    </div> -->
          <div class="comment-form">
            <h3 class="comment-one__block-title">Leave a Comment</h3><!-- /.comment-one__block-title -->
            <form action="#" class="contact-one__form">
              <div class="row">
                <div class="col-lg-6">
                  <div class="input-box">
                    <input type="text" placeholder="name" name="name">
                  </div>
                </div><!-- /.col-lg-6 -->
                <div class="col-lg-6">
                  <div class="input-box">
                    <input type="text" placeholder="Email" name="email">
                  </div>
                </div><!-- /.col-lg-6 -->
                <div class="col-lg-6">
                  <div class="input-box">
                    <input type="text" placeholder="Phone" name="number">
                  </div>
                </div><!-- /.col-lg-6 -->
                <div class="col-lg-6">
                  <div class="input-box">
                    <input type="text" placeholder="Subject" name="subject">
                  </div>
                </div><!-- /.col-lg-6 -->
                <div class="col-lg-12">
                  <div class="input-box">
                    <textarea placeholder="Message" name="message"></textarea>
                  </div>
                </div><!-- /.col-lg-12 -->
                <div class="col-lg-12 text-left">
                  <div class="input-box">
                    <button type="submit" class="main-btn main-btn-2">Send message</button>
                  </div>
                  <!-- /.thm-btn contact-one__btn -->
                </div><!-- /.col-lg-12 -->
              </div><!-- /.row -->
            </form><!-- /.contact-one__form -->
          </div><!-- /.comment-form -->
        </div><!-- /.col-lg-8 -->
        <div class="col-lg-4 col-md-6 col-sm-7">
          <div class="sidebar">
            <!-- <div class="sidebar__single sidebar__search">
              <form action="#" class="sidebar__search-form">
                <input type="text" name="search" placeholder="Search here...">
                <button type="submit"><i class="fa fa-search"></i></button>
              </form>
            </div>/.sidebar__single -->
            <!-- <div class="sidebar__single sidebar__category">
              <h3 class="sidebar__title">Categories</h3>/.sidebar__title -->
              <!-- <ul class="sidebar__category-list">
                <li class="sidebar__category-list-item"><a href="#">Business <i class="fa fa-angle-right"></i></a></li>
                <li class="sidebar__category-list-item"><a href="#">Coworking <i class="fa fa-angle-right"></i></a></li>
                <li class="sidebar__category-list-item"><a href="#">Freelancers <i class="fa fa-angle-right"></i></a></li>
                <li class="sidebar__category-list-item"><a href="#">Creative people <i class="fa fa-angle-right"></i></a></li>
                <li class="sidebar__category-list-item"><a href="#">Technology <i class="fa fa-angle-right"></i></a></li>
                <li class="sidebar__category-list-item"><a href="#">Startups <i class="fa fa-angle-right"></i></a></li>
              </ul></.sidebar__category-list -->
         <!--    </div>/.sidebar__single -->
            <div class="sidebar__single sidebar__post">
              <h3 class="sidebar__title">Recent Posts</h3><!-- /.sidebar__title -->
              <div class="sidebar__post-wrap">
                <div class="sidebar__post__single" v-for="item in others">
                  <div class="sidebar__post-image">
                    <div class="inner-block"><img :src="`${img}/uploads/${item.main_image}`"  alt="Awesome Image" style="width: 69px; height: 69px;"></div>
                    <!-- /.inner-block -->
                  </div><!-- /.sidebar__post-image -->
                  <div class="sidebar__post-content">
                    <h4 class="sidebar__post-title"> 
                       <a    :to="{ path: '/single-news', query: { id: item.id } }" v-on:click="setID(item.id)">{{item.title}}</a></h4>
                    <!-- /.sidebar__post-title -->
                  </div><!-- /.sidebar__post-content -->
                </div><!-- /.sidebar__post__single -->
                
                
              </div><!-- /.sidebar__post-wrap -->
            </div><!-- /.sidebar__single -->
            <!-- /.sidebar__single -->
          </div><!-- /.sidebar -->
        </div><!-- /.col-lg-4 -->
      </div><!-- /.row -->
    </div><!-- /.container -->
  </section>
</template>

<script>
   import {url} from '../data/api';
   import {img} from '../data/api'
             // window.location.reload(true)

    export default {

        name: "BlogDetails",
        data() {
          return {
            data: null,
            others: null,
            img:img,
            id:null
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
            const response = await fetch(`${url}/blogs/view/${this.id}`, {
                    method : "GET",
                });
                const res = await response.json();
                this.data = await res.data;
                console.log(this.data)
                console.log(this.data.id)
                console.log(this.$route.query.id)

                
                //  window.location.reload(true)

          }, 
          async fetchOthers() {      
            const response = await fetch(`${url}/blogs/others/${this.id}`, {
                    method : "GET",
                });
                const res = await response.json();
                this.others = await res.data;
                console.log(this.others)
          },    

          setID(id){
            this.id = id;
            console.log(id)
            this.fetchData();
            this.fetchOthers();  

          }
      },
        async mounted(){
          this.fetchData();   
          this.fetchOthers();  
          console.log(this.data); 
          
    },
    created() {
      this.id = this.$route.query.id
    }  
    }
</script>

<style scoped>

</style>
