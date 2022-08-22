<template>
  <div id="index" class="main-banner">
    <swiper
        :slides-per-view="1"
        :space-between="50"
        :autoplay="{ delay: 2500, disableOnInteraction: false,}"
        :loop="true"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
    >
      <swiper-slide  v-for="(data,index) in SwiperData" :key="index">
          <div class="swipe-slider-wrapper">
              <div class="container">
                  <div class="row align-items-center">
                      <div class="col-12 col-sm-12 col-md-6 col-lg-6">
                          <div class="slider-image"> 
                              <img :src="require(`../assets/images/${data.image}`)" class="img-fluid" />
                          </div>
                          <!-- slider-image -->
                      </div>
                      <!-- col-12 col-sm-12 col-md-6 col-lg-6 -->
                      <div class="col-12 col-sm-12 col-md-6 col-lg-6">
                          <div class="swiper-slider-right">
                              <h2 class="text-capitalize">{{data.heading}}</h2>
                              <p class="">{{ data.paragraph }}</p>
                              <button >Reach Us <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="var(--tq-white)" class="bi bi-arrow-right-circle" viewBox="0 0 16 16" data-v-609fb42c=""><path fill-rule="evenodd" d="M1 8a7 7 0 1 0 14 0A7 7 0 0 0 1 8zm15 0A8 8 0 1 1 0 8a8 8 0 0 1 16 0zM4.5 7.5a.5.5 0 0 0 0 1h5.793l-2.147 2.146a.5.5 0 0 0 .708.708l3-3a.5.5 0 0 0 0-.708l-3-3a.5.5 0 1 0-.708.708L10.293 7.5H4.5z" data-v-609fb42c=""></path></svg></button>
                          </div>
                          <!-- d-flex align-items-center -->
                      </div>
                      <!-- col-12 col-sm-12 col-md-6 col-lg-6 -->
                  </div>
                  <!-- row -->
              </div>
              <!-- conatiner -->
          </div>
          <!-- swipe-slider-wrapper -->
      </swiper-slide>
    </swiper>
</div>
<!-- main-banner -->

<div class="color-bar mt-4">
          <div class="inner-bar"></div>
      </div>
      <!-- color-bar -->

<div id="about" class="about-us" v-for="(data,key) in AboutData" :key="key">
    <div class="container-fluid">
        <div class="row align-items-center flex-lg-row-reverse">
            <div class="col-12 col-md-12 col-lg-5">
              <div class="about-us-images d-flex align-items-center justify-content-center position-relative">
                  <div class="row">
                      <div class="col-6 col-md-6 col-lg-6">
                          <div class="about-image-show">
                              <img src="../assets/images/about-1.jpg" alt="about-us" class="img-fluid" />
                          </div>
                          <!-- about-image-show -->
                      </div>
                      <div class="col-6 col-md-6 col-lg-6">
                          <div class="about-image-show">
                               <img src="../assets/images/about-2.jpg" alt="about-us" class="img-fluid about-image-2" />
                          </div>
                          <!-- about-image-show -->
                      </div>
                      <div class="col-12 col-md-12 col-lg-12">
                        <div class="about-image-show about-image-three">
                              <img src="../assets/images/about-3.jpg" alt="about-us" class="img-fluid" />
                          </div>
                          <!-- about-image-show -->
                      </div>
                  </div>
                  <div class="about-us-icon position-absolute rounded-pill">
                      <h3>
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="90" height="90" style="fill: var(--tq-orange);"><path d="M15 11h7v2h-7zm1 4h6v2h-6zm-2-8h8v2h-8zM4 19h10v-1c0-2.757-2.243-5-5-5H7c-2.757 0-5 2.243-5 5v1h2zm4-7c1.995 0 3.5-1.505 3.5-3.5S9.995 5 8 5 4.5 6.505 4.5 8.5 6.005 12 8 12z"></path></svg>
                      </h3>
                  </div>
              <!-- about-us-icon -->
              </div>
              <!-- about-us-images -->
              
            </div>
            <!-- col-12 col-md-5 -->
            <div class="col-12 col-md-12 col-lg-5">
                <div class="about-content">
                    <h4 class="text-capitalize">{{ data.heading }}</h4>
                    <h3>{{ data.captain }}</h3>
                    <p>{{data.firstPara}}</p>
                    <p>{{data.secondPara}}</p>
                    <p>{{data.thirdPara}}</p>
                </div>
                <!-- about-content -->
            </div>
            <!-- col-12 col-md-5 -->
        </div>
        <!-- row -->
    </div>
    <!-- container-fluid -->
</div>
<!-- about-us -->
<div id="OurServices">
  <div class="ourservices"> 
      <div class="container">
        <div class="row">
            <MainHeading heading="our Services" description="The Services That We Provide For Our Ultimate Clients"/>
        </div>
      </div>
      <!-- container -->
  </div>
  <!-- OurServices -->

  <div id="accounting" class="accounting-section">
      <div class="container">
          <div class="row" v-for="(data,value) in AccountingData" :key="value">
              <div class="col-12 col-md-12 col-lg-5 col-xl-4 order-last order-lg-first">
                  <div class="accounting-content mt-5 mt-lg-0">
                      <div class="services-item position-relative">
                          <img :src="require(`../assets/images/${ data.uniqueImage }`)" alt="money-sack" class="img-fluid mb-4" />
                          <h3 class="text-capitalize">{{data.heading}}</h3>
                          <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-white);transform: ;msFilter:;"><path d="M20 6c0-2.168-3.663-4-8-4S4 3.832 4 6v2c0 2.168 3.663 4 8 4s8-1.832 8-4V6zm-8 13c-4.337 0-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3c0 2.168-3.663 4-8 4z"></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.firstPara }}</p>
                          <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-white);transform: ;msFilter:;"><path d="M20 6c0-2.168-3.663-4-8-4S4 3.832 4 6v2c0 2.168 3.663 4 8 4s8-1.832 8-4V6zm-8 13c-4.337 0-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3c0 2.168-3.663 4-8 4z"></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.secondPara }}</p>
                          <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-white);transform: ;msFilter:;"><path d="M20 6c0-2.168-3.663-4-8-4S4 3.832 4 6v2c0 2.168 3.663 4 8 4s8-1.832 8-4V6zm-8 13c-4.337 0-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3c0 2.168-3.663 4-8 4z"></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.thirdPara }}</p>
                          <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-white);transform: ;msFilter:;"><path d="M20 6c0-2.168-3.663-4-8-4S4 3.832 4 6v2c0 2.168 3.663 4 8 4s8-1.832 8-4V6zm-8 13c-4.337 0-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3c0 2.168-3.663 4-8 4z"></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.fourthPara }}</p>
                      </div>
                  </div>
              </div>
              <div class="col-12 col-md-12 col-lg-7 col-xl-7 order-first order-lg-last">
                  <div class="image-services text-center">
                      <img :src="require(`../assets/images/${ data.mainImage }`)" class=""  alt="accounting"/>
                  </div>
                  <!-- image-services -->
              </div>
          </div>
      </div>
  </div>
  <!-- accounting-section -->

  <div id="taxation" class="taxation-section">
      <div class="container">
          <div class="row" v-for="(data,value) in TaxationData" :key="value">
              <div class="col-12 col-md-12 col-lg-7 col-xl-7">
                   <div class="image-services text-center mt-5 mt-xl-0">
                      <img :src="require(`../assets/images/${ data.mainImage }`)" class=""  alt="accounting"/>
                  </div>
                  <!-- image-services -->
              </div>
              <div class="col-12 col-md-12 col-lg-5 col-xl-4">
                <div class="accounting-content">
                      <div class="services-item item-active position-relative mt-5 mt-xl-0">
                          <img :src="require(`../assets/images/${ data.uniqueImage }`)" alt="money-sack" class="img-fluid mb-4" />
                          <h3 class="text-capitalize">{{data.heading}}</h3>
                          <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-orange);transform: ;msFilter:;"><path d="M20 6c0-2.168-3.663-4-8-4S4 3.832 4 6v2c0 2.168 3.663 4 8 4s8-1.832 8-4V6zm-8 13c-4.337 0-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3c0 2.168-3.663 4-8 4z"></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.firstPara }}</p>
                          <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-orange);transform: ;msFilter:;"><path d="M20 6c0-2.168-3.663-4-8-4S4 3.832 4 6v2c0 2.168 3.663 4 8 4s8-1.832 8-4V6zm-8 13c-4.337 0-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3c0 2.168-3.663 4-8 4z"></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.secondPara }}</p>
                          <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-orange);transform: ;msFilter:;"><path d="M20 6c0-2.168-3.663-4-8-4S4 3.832 4 6v2c0 2.168 3.663 4 8 4s8-1.832 8-4V6zm-8 13c-4.337 0-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3c0 2.168-3.663 4-8 4z"></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.thirdPara }}</p>
                      </div>
                  </div>
                 <!-- accounting-content  -->
              </div>
          </div>
      </div>
  </div>
  <!-- taxation-section -->

  <div id="advisory" class="advisory-section">
      <div class="container">
          <div class="row" v-for="(data,value) in AdvisoryData" :key="value">
              <div class="col-12 col-md-12 col-lg-5 col-xl-4 order-last order-lg-first">
                  <div class="accounting-content mt-5 mt-lg-0">
                      <div class="services-item position-relative">
                          <svg class="mb-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="70" height="70" style="fill: var(--tq-white);transform: ;msFilter:;"><path d="M20 12v-1.707c0-4.442-3.479-8.161-7.755-8.29-2.204-.051-4.251.736-5.816 2.256A7.933 7.933 0 0 0 4 10v2c-1.103 0-2 .897-2 2v4c0 1.103.897 2 2 2h2V10a5.95 5.95 0 0 1 1.821-4.306 5.977 5.977 0 0 1 4.363-1.691C15.392 4.099 18 6.921 18 10.293V20h2c1.103 0 2-.897 2-2v-4c0-1.103-.897-2-2-2z"></path><path d="M7 12h2v8H7zm8 0h2v8h-2z"></path></svg>
                          <h3 class="text-capitalize">{{data.heading}}</h3>
                          <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-white);transform: ;msFilter:;"><path d="M20 6c0-2.168-3.663-4-8-4S4 3.832 4 6v2c0 2.168 3.663 4 8 4s8-1.832 8-4V6zm-8 13c-4.337 0-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3c0 2.168-3.663 4-8 4z"></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.firstPara }}</p>
                          <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-white);transform: ;msFilter:;"><path d="M20 6c0-2.168-3.663-4-8-4S4 3.832 4 6v2c0 2.168 3.663 4 8 4s8-1.832 8-4V6zm-8 13c-4.337 0-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3c0 2.168-3.663 4-8 4z"></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.secondPara }}</p>
                          <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-white);transform: ;msFilter:;"><path d="M20 6c0-2.168-3.663-4-8-4S4 3.832 4 6v2c0 2.168 3.663 4 8 4s8-1.832 8-4V6zm-8 13c-4.337 0-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3c0 2.168-3.663 4-8 4z"></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.thirdPara }}</p>
                          <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-white);transform: ;msFilter:;"><path d="M20 6c0-2.168-3.663-4-8-4S4 3.832 4 6v2c0 2.168 3.663 4 8 4s8-1.832 8-4V6zm-8 13c-4.337 0-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3c0 2.168-3.663 4-8 4z"></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.fourthPara }}</p>
                      </div>
                  </div>
              </div>
              <div class="col-12 col-md-12 col-lg-7 col-xl-7 order-first order-lg-last">
                  <div class="image-services text-center">
                      <img :src="require(`../assets/images/${ data.mainImage }`)" class=""  alt="accounting"/>
                  </div>
                  <!-- image-services -->
              </div>
          </div>
      </div>
  </div>
  <!-- accounting-section -->
</div>
<!-- OurServices -->

<div id="business-support" class="bus-support">
    <div class="container">
      <div class="row">
        <div class="col-12 col-md-12 col-lg-12">
            <div class="services-description text-center mb-5">
                <h4 class="text-capitalize">business</h4>
                <h3 class="business-description">Business support</h3>
            </div>
            <!-- services-description -->
        </div>
        <div class="col-12 col-lg-7">
            <div class="support-image text-center">
              <img src="../assets/images/support.jpg" alt="business-support" class="img-fluid"/>
            </div>
        </div>
        <div class="col-12 col-lg-5">
          <div class="list-container">
            <div class="row align-items-center support-lists-row" v-for="(data,index) in businessSupport" :key="index">
                <div class="col-lg-3">
                  <div class="list-svg">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="60" height="60" style="fill: var(--tq-orange);">
                      <path :d="data.path"></path>
                    </svg>
                  </div>
                  <!-- list-image -->
                </div>
                <div class="col-lg-9">
                  <div class="support-content">
                    <h3 class="text-capitalize">{{data.heading}}</h3>
                    <p class="mb-0">{{data.description}}</p>
                  </div>
                </div>
            </div>
          </div>
          <!-- list-container -->
        </div>
      </div>
      <!-- row -->
    </div>
    <!-- container -->
</div>
<!-- bus-support -->

<div id="testimonials" class="testimonial">
    <div class="container">
      <div class="row">
        <MainHeading heading="testimonials" description="See What Our Client's Say About Our Work" />
        <div class="col-12 col-lg-12">
          <div class="testimonial-carousel">
              <swiper
                :slides-per-view="1"
                @swiper="onSwiper"
                @slideChange="onSlideChange"
                :autoplay="{delay:2000, disableOnInteraction: false,}"
                :navigation="true"
                :modules="modules"
                :loop="true"
                :pagination="{clickable: true,}"
              >
                <swiper-slide v-for="(data,index) in Testimonial" :key="index">
                    <div class="testimonial-section">
                        <div class="container">
                          <div class="row justify-content-center">
                              <div class="col-md-8 col-lg-8">
                                  <div class="all-testimonials text-center">
                                      <svg class="mb-3" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="60" height="60" style="fill: var(--tq-orange);"><path :d=data.path></path></svg>
                                      <p>{{data.content}}</p>
                                      <div class="client">
                                          <img src="../assets/images/client.jpg" alt="client" class="img-fluid rounded-pill" />
                                          <p>{{data.client}}</p>
                                      </div>
                                      <!-- client -->
                                  </div>
                                  <!-- all-testimonials -->
                              </div>
                          </div>
                        </div>
                    </div>
                    <!-- testimonial-section -->
                </swiper-slide>
              </swiper>
          </div>
        </div>
      </div>
    </div>
</div>
<!-- testimonials -->

<div id="useful-link" class="useful-links about-us">
    <div class="container">
      <div class="row justify-content-center">
          <MainHeading heading="links" description="Useful Links"/>
      </div>
      <div class="row justify-content-center" v-for="(data,value) in UsefulLinksData" :key="value">          
            <div class="col-md-6 col-lg-4">
                <div class="accounting-content">
                    <div class="services-item item-active position-relative mt-5 mt-xl-0">
                      <svg class="mb-3" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="90" height="90" style="fill: var(--tq-orange);">
                      <path :d=data.uniquepath></path>
                      </svg>
                        <!-- <img :src="require(`../assets/images/${ data.uniqueImage }`)" alt="money-sack" class="img-fluid mb-4" /> -->
                        <h3 class="text-capitalize">{{data.heading}}</h3>
                        <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-orange);transform: ;msFilter:;"><path :d=data.commonPath></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.firstPara }}</p>
                        <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-orange);transform: ;msFilter:;"><path :d=data.commonPath></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.secondPara }}</p>
                        <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-orange);transform: ;msFilter:;"><path :d=data.commonPath></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.thirdPara }}</p>
                        <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-orange);transform: ;msFilter:;"><path :d=data.commonPath></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.fourthPara }}</p>
                    </div>
                </div>
                <!-- accounting-content  -->
          </div>
          <div class="col-md-6 col-lg-4">
              <div class="useful-image text-center mt-5 mt-xl-0">
                  <img :src="require(`../assets/images/${ data.mainImage }`)" class=""  alt="accounting"/>
              </div>
          </div>

      </div>
    </div>
</div>
<!-- useful-links -->
<div id="ContactUs" class="contact-us">
    <div class="container">
      <div class="row">
          <MainHeading heading="inquery" description="Get in Touch" />
      </div>
      <!-- row -->
      <div class="inquery">
        <div class="row align-items-center">
            <div class="col-12 col-md-6 col-lg-3">
                <div class="inquery-image">
                    <img src="../assets/images/contact-us.png" alt="inquery-boy" class="img-fluid" />
                </div>
                <!-- inquery-image -->
            </div>
            <div class="col-12 col-md-6 col-lg-3">
                <div class="find-us" v-for="(data,index) in Inquery" :key="index">
                    <h2 class="d-flex align-items-center justify-content-between"><svg class="rounded-pill" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="45" height="45" style="fill: var(--tq-white); padding: 9px; background-color: var(--tq-red);"><path :d=data.path></path></svg>
                    <span class="text-uppercase">{{data.heading}}</span>
                    </h2>
                    <p class="mb-0 text-center">{{data.caption}}</p>
                </div>
            </div>
            <div class="col-12 col-md-12 col-lg-6">
                <div class="contact-form">
                    <form>
                        <div class="row">
                          <div class="col-12 col-md-6 col-lg-6">
                                <div class="input-area">
                                    <input type="text" name="username" placeholder="Name">
                                </div>
                            </div>
                          <div class="col-12 col-md-6 col-lg-6">
                              <div class="input-area">
                                  <input type="text" name="email" placeholder="Email">
                              </div>
                          </div>
                          <div class="col-12 col-md-6 col-lg-6">
                                <div class="input-area">
                                    <input type="number" name="number" placeholder="Number">
                                </div>
                            </div>
                          <div class="col-12 col-md-6 col-lg-6">
                              <div class="input-area">
                                  <input type="text" name="subject" placeholder="Subject">
                              </div>
                          </div>
                          <div class="col-12 col-md-12 col-lg-12">
                                <div class="input-area">
                                  <textarea name="message" id="" rows="10"></textarea>
                                  <button type="submit" class="text-capitalize">send message</button>
                              </div>
                          </div>
                        </div>
                    </form>
                </div>
                <!-- contact-form -->
            </div>
        </div>
      </div>
      <!-- inquery  -->
    </div>
</div>
<!-- contact-us -->

<div id="faq" class="questions">
      <div class="container">
          <div class="row">
              <MainHeading heading="faq" description="Frequently Asked Questions" />
          </div>
          <div class="row justify-content-center">
              <div class="col-12 col-md-12 col-lg-8">
                  <div class="accordion-custom">
                      <div class="accordion" id="accordionFaq">
                            <div class="accordion-item">
                                <h2 class="accordion-header" id="headingOne">
                                    <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                                      Why Accounting Matters for Your Small Business? 
                                    </button>
                                </h2>
                                <div id="collapseOne" class="accordion-collapse collapse show" aria-labelledby="headingOne" data-bs-parent="#accordionFaq">
                                    <div class="accordion-body">
                                        <div class="accordion-inside">
                                            <p>Becoming an entrepreneur is not easy. It doesn't matter if you are the owner of a small business or a large company. Most entrepreneurs have the problem of lack of funds. This means they need to look for some departments of the company. Accounting delays can be a catastrophic problem for a company, as so many things are happening.</p>
                                            <p>In case, accounting services help business owners check the financial performance of the business. It gives information about P&L, liabilities, earnings, costs in a business. From holding accounting records for a variety of purposes, including-</p>
                                            <ul class="m-0 p-0"> 
                                              <li class="text-capitalize">it helps plan for growth</li>
                                              <li class="text-capitalize">to attract investors</li>
                                              <li class="text-capitalize">to gets you paid</li>
                                              <li class="text-capitalize">accounting keeps you on top of debts</li>
                                              <li class="text-capitalize">pay the right amount of taxes</li>
                                              
                                            </ul>
                                        </div>
                                      <!-- accordion-inside -->
                                    </div>
                                </div>
                            </div>
                            <div class="accordion-item">
                                <h2 class="accordion-header" id="headingTwo">
                                    <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                                      What are the Benefits of Accounting Services for Business?
                                    </button>
                                </h2>
                                <div id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingTwo" data-bs-parent="#accordionFaq">
                                    <div class="accordion-body">
                                        <div class="accordion-inside">
                                            <p>Many business owners choose to manage their internal accounting costs. Doing so is prone to many problems- wasting valuable resources and increasing vulnerabilities. Therefore, it can bring many pain points to the success of your business. So talk to an accounting professional with over 100 organisations across Canada.</p>
                                            <p>We are a growing accounting business with a focus on accounting services. Our expertise extends from account management to tax credits. You can focus on what's important to your business growth with Teqo Accounting.</p>
                                            <p>Does your company meet accounting requirements? If not, please let us know. At Teqo Accounting, we are a corporate accounting partner. The main benefits of accounting services are:</p>
                                            <ul class="m-0 p-0"> 
                                              <li>It facilitates the business growth</li>
                                              <li>Huge savings from higher deductions</li>
                                              <li>Increase profitability</li>
                                              <li>Reduce cost</li>
                                              <li>Minimize risk</li>
                                              <li>Better business decisions</li>
                                              <li>Check total compliance with statutory regulations & requirements</li>
                                            </ul>
                                        </div>
                                      <!-- accordion-inside -->
                                    </div>
                                </div>
                            </div>
                            <div class="accordion-item">
                                <h2 class="accordion-header" id="headingThree">
                                    <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                                      Reasons Why Every Business Needs Accounting and Tax Services?
                                    </button>
                                </h2>
                                <div id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree" data-bs-parent="#accordionFaq">
                                    <div class="accordion-body">
                                        <div class="accordion-inside">
                                            <p>The days when companies had accounting books and files are over. From today, the internet is happening for everything. This changed the concept of accounting firm accounts. Now you need the best bookkeeping professionals to accomplish your account. Professional accountants go beyond just bookkeeping. They facilitate the financial processing and planning of the company.</p>
                                            <p>To improve cash flow and management, Teqo Accounting has a team of experienced professionals who manage your account. See this article for the main reasons why you need accounting services-</p>
                                            <ul class="m-0 p-0"> 
                                              <li class="text-capitalize">foster business growth</li>
                                              <li class="text-capitalize">maximize the savings & deductions</li>
                                              <li class="text-capitalize">tracking expenses</li>
                                              <li class="text-capitalize">tax services</li>
                                              
                                            </ul>
                                        </div>
                                      <!-- accordion-inside -->
                                    </div>
                                </div>
                            </div>
                            <div class="accordion-item">
                                <h2 class="accordion-header" id="headingOne">
                                    <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseFour" aria-expanded="true" aria-controls="collapseFour">
                                      What are the accounting services included?
                                    </button>
                                </h2>
                                <div id="collapseFour" class="accordion-collapse collapse" aria-labelledby="headingFour" data-bs-parent="#accordionFaq">
                                    <div class="accordion-body">
                                        <div class="accordion-inside">
                                            <p>Starting a business requires a lot of accounting calculations. This is done daily, from transaction recording to expense planning. You have to do a certain amount of bookkeeping to run your business. No matter what your business is, accounting is messed up. It rarely damages your daily record.</p>
                                            <p>This is the right time to let accounting professionals work for you.Teqo Accounting is a team of brilliant people to figure out the most how to do things. We can make accounting manageable. Our team takes care of finance with strategic planning. We are focused on the following financial aspects of your business-</p>
                                            <ul class="m-0 p-0"> 
                                              <li class="text-capitalize">tax accounting services</li>
                                              <li class="text-capitalize">CFO services</li>
                                              <li class="text-capitalize">bookkeeping</li>
                                              <li class="text-capitalize">bank reconciliation</li>
                                              <li class="text-capitalize">payroll processing</li>
                                              <li class="text-capitalize">accounts receivable</li>
                                              <li class="text-capitalize">payable accounts</li>
                                            </ul>
                                        </div>
                                      <!-- accordion-inside -->
                                    </div>
                                </div>
                            </div>
                      </div>
                  </div>
              </div>
          </div>
      </div>
  </div>
<!-- faq -->
<div id="WhatsApp" class="whatsapp">
  <a href="">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="35" height="35" style="fill: var(--tq-white);"><path fill-rule="evenodd" clip-rule="evenodd" d="M18.403 5.633A8.919 8.919 0 0 0 12.053 3c-4.948 0-8.976 4.027-8.978 8.977 0 1.582.413 3.126 1.198 4.488L3 21.116l4.759-1.249a8.981 8.981 0 0 0 4.29 1.093h.004c4.947 0 8.975-4.027 8.977-8.977a8.926 8.926 0 0 0-2.627-6.35m-6.35 13.812h-.003a7.446 7.446 0 0 1-3.798-1.041l-.272-.162-2.824.741.753-2.753-.177-.282a7.448 7.448 0 0 1-1.141-3.971c.002-4.114 3.349-7.461 7.465-7.461a7.413 7.413 0 0 1 5.275 2.188 7.42 7.42 0 0 1 2.183 5.279c-.002 4.114-3.349 7.462-7.461 7.462m4.093-5.589c-.225-.113-1.327-.655-1.533-.73-.205-.075-.354-.112-.504.112s-.58.729-.711.879-.262.168-.486.056-.947-.349-1.804-1.113c-.667-.595-1.117-1.329-1.248-1.554s-.014-.346.099-.458c.101-.1.224-.262.336-.393.112-.131.149-.224.224-.374s.038-.281-.019-.393c-.056-.113-.505-1.217-.692-1.666-.181-.435-.366-.377-.504-.383a9.65 9.65 0 0 0-.429-.008.826.826 0 0 0-.599.28c-.206.225-.785.767-.785 1.871s.804 2.171.916 2.321c.112.15 1.582 2.415 3.832 3.387.536.231.954.369 1.279.473.537.171 1.026.146 1.413.089.431-.064 1.327-.542 1.514-1.066.187-.524.187-.973.131-1.067-.056-.094-.207-.151-.43-.263"></path></svg>
  </a>
</div>

</template>

<script>
// @ is an alias to /src
// Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from "swiper/vue";
  import 'swiper/css';
  import 'swiper/css/navigation';
  import "swiper/css/autoplay";
// Import components 
  import MainHeading from '../components/Landing/MainHeading.vue'
export default {
  name: 'HomePage',
  components: {
      Swiper, 
      SwiperSlide,
      MainHeading
    },
    data(){
        return{
            SwiperData:[
                {
                    image: 'taxation.png',
                    heading: 'taxation',
                    paragraph: 'From accounting to tax filing, it’s a game of numbers. Don’t worry! We will keep your business numbers managed.',
                },
                {
                    image: 'advisory.png',
                    heading: 'business advisory / support',
                    paragraph: 'Teqo Accounting is a best-in-class accounting advisory service provider to help businesses to grow.',
                },
                {
                    image: 'accounting.png',
                    heading: 'accounting',
                    paragraph: 'We will handle the accounting aspect of your business, while letting you focus on your business.',
                },
            ],
            AboutData:[
                {
                    heading: 'about',
                    captain: 'We committed to your Success',
                    firstPara: 'Teqo accounting is a firm based in Surrey, BC which is a trusted bookkeeping, tax and accounting services provider for small to medium sized enterprises across British Columbia.',
                    secondPara: 'Our experienced staff is capable to handle the accounting aspect of your business, while letting you focus on your business.',
                    thirdPara: "Teqo Accounting provides dedicated bookkeeping support with a set of unique features and it doesn't matter how complex is your accounting."
                }
            ],
            AccountingData : [
                {
                    uniqueImage : 'money-sack.png',
                    heading : 'accounting',
                    firstPara : 'Bookkeeping',
                    secondPara : 'GST/ PST Returns',
                    thirdPara : 'Payroll',
                    fourthPara : 'Notice to Reader compilation Engagements', 
                    mainImage: 'service-accounting.png',
                }
            ],
            TaxationData : [
                {
                    uniqueImage : 'tax.png',
                    heading : 'taxation',
                    firstPara : 'Personal Tax Returns',
                    secondPara : 'Corporate Tax Returns',
                    thirdPara : 'Tax Planing',
                    mainImage: 'service-taxation.png',
                }
            ],
            AdvisoryData : [
                {
                    heading : 'business advisory / support',
                    firstPara : 'Business Plans and evolutions',
                    secondPara : 'Assistance with Starting a business',
                    thirdPara : 'Company formation/ GST PST Registration / WCB Registration/ Payroll Registration',
                    fourthPara : 'Finance Sourcing', 
                    mainImage: 'service-advisory.png',
                }
            ],
            businessSupport: [
              {
                path: 'M5 8.999a6.99 6.99 0 0 0 2.879 5.646l.001.001a6.972 6.972 0 0 0 1.881.979l.051.019a6.906 6.906 0 0 0 1.163.271 6.79 6.79 0 0 0 1.024.085H12c.35 0 .69-.034 1.027-.084l.182-.028c.336-.059.664-.139.981-.243l.042-.016C17 14.693 19 12.078 19 8.999 19 5.14 15.86 2 12 2S5 5.14 5 8.999zM12 4c2.756 0 5 2.242 5 4.999h-2A3.003 3.003 0 0 0 12 6V4zM7.521 16.795V22L12 20.5l4.479 1.5.001-5.205a8.932 8.932 0 0 1-8.959 0z',
                heading: 'business registration',
                description: 'Sole-proprietor, Partnership & corporation, Payroll/GST/HST setup.',
              },
              {
                path: 'M8 12.052c1.995 0 3.5-1.505 3.5-3.5s-1.505-3.5-3.5-3.5-3.5 1.505-3.5 3.5 1.505 3.5 3.5 3.5zM9 13H7c-2.757 0-5 2.243-5 5v1h12v-1c0-2.757-2.243-5-5-5zm11.294-4.708-4.3 4.292-1.292-1.292-1.414 1.414 2.706 2.704 5.712-5.702z',
                heading: 'assistance',
                description: 'Help with availing federal and provincial grants for individuals and businesses like CRB, business, wage and rent subsidies.',
              },
              {
                path: 'M3 5v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2V5a2 2 0 0 0-2-2H5a2 2 0 0 0-2 2zm7 2h8v2h-8V7zm0 4h8v2h-8v-2zm0 4h8v2h-8v-2zM6 7h2v2H6V7zm0 4h2v2H6v-2zm0 4h2v2H6v-2z',
                heading: 'business plans',
                description: 'Research based customized business plans for entrepreneur and business visas',
              },
              {
                path: 'M12 2C6.486 2 2 6.486 2 12s4.486 10 10 10 10-4.486 10-10S17.514 2 12 2zm1 14.915V18h-2v-1.08c-2.339-.367-3-2.002-3-2.92h2c.011.143.159 1 2 1 1.38 0 2-.585 2-1 0-.324 0-1-2-1-3.48 0-4-1.88-4-3 0-1.288 1.029-2.584 3-2.915V6.012h2v1.109c1.734.41 2.4 1.853 2.4 2.879h-1l-1 .018C13.386 9.638 13.185 9 12 9c-1.299 0-2 .516-2 1 0 .374 0 1 2 1 3.48 0 4 1.88 4 3 0 1.288-1.029 2.584-3 2.915z',
                heading: 'payroll',
                description: 'Payroll management, support with payroll, payroll taxes, generating T4s',
              }

            ],
            Testimonial: [
              {
                content: "Hi, I'm Robert. I run my own business and I have a huge company. However, owning a large company makes it pathetic to organize employees and plan viable strategies. Busy doing these things, I don't have time to manage my company account. Thanks to the Teqo Accounting software, which makes it easy to track accounting reports and profitability out of the box..",
                client: 'Robert',
                path: 'm21.95 8.721-.025-.168-.026.006A4.5 4.5 0 1 0 17.5 14c.223 0 .437-.034.65-.065-.069.232-.14.468-.254.68-.114.308-.292.575-.469.844-.148.291-.409.488-.601.737-.201.242-.475.403-.692.604-.213.21-.492.315-.714.463-.232.133-.434.28-.65.35l-.539.222-.474.197.484 1.939.597-.144c.191-.048.424-.104.689-.171.271-.05.56-.187.882-.312.317-.143.686-.238 1.028-.467.344-.218.741-.4 1.091-.692.339-.301.748-.562 1.05-.944.33-.358.656-.734.909-1.162.293-.408.492-.856.702-1.299.19-.443.343-.896.468-1.336.237-.882.343-1.72.384-2.437.034-.718.014-1.315-.028-1.747a7.028 7.028 0 0 0-.063-.539zm-11 0-.025-.168-.026.006A4.5 4.5 0 1 0 6.5 14c.223 0 .437-.034.65-.065-.069.232-.14.468-.254.68-.114.308-.292.575-.469.844-.148.291-.409.488-.601.737-.201.242-.475.403-.692.604-.213.21-.492.315-.714.463-.232.133-.434.28-.65.35l-.539.222c-.301.123-.473.195-.473.195l.484 1.939.597-.144c.191-.048.424-.104.689-.171.271-.05.56-.187.882-.312.317-.143.686-.238 1.028-.467.344-.218.741-.4 1.091-.692.339-.301.748-.562 1.05-.944.33-.358.656-.734.909-1.162.293-.408.492-.856.702-1.299.19-.443.343-.896.468-1.336.237-.882.343-1.72.384-2.437.034-.718.014-1.315-.028-1.747a7.571 7.571 0 0 0-.064-.537z'
              },
              {
                content: "In this expensive world, every business owner is looking for smart and budgeted book-keeping solutions. Hiring a team of accountants can be expensive for business. That's why I choose Teqo accounting software. It’s an ai accounting tool that allows business owners to manage expenses, pay bills or collect receipts under one roof.",
                client: 'John',
                path: 'm21.95 8.721-.025-.168-.026.006A4.5 4.5 0 1 0 17.5 14c.223 0 .437-.034.65-.065-.069.232-.14.468-.254.68-.114.308-.292.575-.469.844-.148.291-.409.488-.601.737-.201.242-.475.403-.692.604-.213.21-.492.315-.714.463-.232.133-.434.28-.65.35l-.539.222-.474.197.484 1.939.597-.144c.191-.048.424-.104.689-.171.271-.05.56-.187.882-.312.317-.143.686-.238 1.028-.467.344-.218.741-.4 1.091-.692.339-.301.748-.562 1.05-.944.33-.358.656-.734.909-1.162.293-.408.492-.856.702-1.299.19-.443.343-.896.468-1.336.237-.882.343-1.72.384-2.437.034-.718.014-1.315-.028-1.747a7.028 7.028 0 0 0-.063-.539zm-11 0-.025-.168-.026.006A4.5 4.5 0 1 0 6.5 14c.223 0 .437-.034.65-.065-.069.232-.14.468-.254.68-.114.308-.292.575-.469.844-.148.291-.409.488-.601.737-.201.242-.475.403-.692.604-.213.21-.492.315-.714.463-.232.133-.434.28-.65.35l-.539.222c-.301.123-.473.195-.473.195l.484 1.939.597-.144c.191-.048.424-.104.689-.171.271-.05.56-.187.882-.312.317-.143.686-.238 1.028-.467.344-.218.741-.4 1.091-.692.339-.301.748-.562 1.05-.944.33-.358.656-.734.909-1.162.293-.408.492-.856.702-1.299.19-.443.343-.896.468-1.336.237-.882.343-1.72.384-2.437.034-.718.014-1.315-.028-1.747a7.571 7.571 0 0 0-.064-.537z'
              },
              {
                content: "I am very pleased to tell you about one of excellent accounting software, Teqo accounting. Now, you don’t need to find accounting books to see previous records. You can get quick access to track your estimation progress. This software allows sending automatic reports on a specific set of times- quarterly, weekly, monthly, etc.",
                client: 'Dawayne',
                path: 'm21.95 8.721-.025-.168-.026.006A4.5 4.5 0 1 0 17.5 14c.223 0 .437-.034.65-.065-.069.232-.14.468-.254.68-.114.308-.292.575-.469.844-.148.291-.409.488-.601.737-.201.242-.475.403-.692.604-.213.21-.492.315-.714.463-.232.133-.434.28-.65.35l-.539.222-.474.197.484 1.939.597-.144c.191-.048.424-.104.689-.171.271-.05.56-.187.882-.312.317-.143.686-.238 1.028-.467.344-.218.741-.4 1.091-.692.339-.301.748-.562 1.05-.944.33-.358.656-.734.909-1.162.293-.408.492-.856.702-1.299.19-.443.343-.896.468-1.336.237-.882.343-1.72.384-2.437.034-.718.014-1.315-.028-1.747a7.028 7.028 0 0 0-.063-.539zm-11 0-.025-.168-.026.006A4.5 4.5 0 1 0 6.5 14c.223 0 .437-.034.65-.065-.069.232-.14.468-.254.68-.114.308-.292.575-.469.844-.148.291-.409.488-.601.737-.201.242-.475.403-.692.604-.213.21-.492.315-.714.463-.232.133-.434.28-.65.35l-.539.222c-.301.123-.473.195-.473.195l.484 1.939.597-.144c.191-.048.424-.104.689-.171.271-.05.56-.187.882-.312.317-.143.686-.238 1.028-.467.344-.218.741-.4 1.091-.692.339-.301.748-.562 1.05-.944.33-.358.656-.734.909-1.162.293-.408.492-.856.702-1.299.19-.443.343-.896.468-1.336.237-.882.343-1.72.384-2.437.034-.718.014-1.315-.028-1.747a7.571 7.571 0 0 0-.064-.537z'
              }
            ],
            UsefulLinksData: [
              {
                uniquepath : 'M12 2C6.486 2 2 6.486 2 12s4.486 10 10 10 10-4.486 10-10S17.514 2 12 2zm7.931 9h-2.764a14.67 14.67 0 0 0-1.792-6.243A8.013 8.013 0 0 1 19.931 11zM12.53 4.027c1.035 1.364 2.427 3.78 2.627 6.973H9.03c.139-2.596.994-5.028 2.451-6.974.172-.01.344-.026.519-.026.179 0 .354.016.53.027zm-3.842.7C7.704 6.618 7.136 8.762 7.03 11H4.069a8.013 8.013 0 0 1 4.619-6.273zM4.069 13h2.974c.136 2.379.665 4.478 1.556 6.23A8.01 8.01 0 0 1 4.069 13zm7.381 6.973C10.049 18.275 9.222 15.896 9.041 13h6.113c-.208 2.773-1.117 5.196-2.603 6.972-.182.012-.364.028-.551.028-.186 0-.367-.016-.55-.027zm4.011-.772c.955-1.794 1.538-3.901 1.691-6.201h2.778a8.005 8.005 0 0 1-4.469 6.201z',
                heading : 'useful links',
                firstPara : 'CRA Canada',
                secondPara : 'Bank of Canada',
                thirdPara : 'Online Payroll Deduction Calculator',
                fourthPara : 'WorkSafe BC',
                mainImage: 'useful-bg.png',
                commonPath: 'M20 6c0-2.168-3.663-4-8-4S4 3.832 4 6v2c0 2.168 3.663 4 8 4s8-1.832 8-4V6zm-8 13c-4.337 0-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3c0 2.168-3.663 4-8 4z'
              }
            ],
            Inquery: [
              {
                path: 'M12 2C7.589 2 4 5.589 4 9.995 3.971 16.44 11.696 21.784 12 22c0 0 8.029-5.56 8-12 0-4.411-3.589-8-8-8zm0 12c-2.21 0-4-1.79-4-4s1.79-4 4-4 4 1.79 4 4-1.79 4-4 4z',
                heading: 'find us',
                caption: '7404 king George Blvd suite 200 surrey British Columbia V3W 1N6 Canada',
              },
              {
                path: 'm20.487 17.14-4.065-3.696a1.001 1.001 0 0 0-1.391.043l-2.393 2.461c-.576-.11-1.734-.471-2.926-1.66-1.192-1.193-1.553-2.354-1.66-2.926l2.459-2.394a1 1 0 0 0 .043-1.391L6.859 3.513a1 1 0 0 0-1.391-.087l-2.17 1.861a1 1 0 0 0-.29.649c-.015.25-.301 6.172 4.291 10.766C11.305 20.707 16.323 21 17.705 21c.202 0 .326-.006.359-.008a.992.992 0 0 0 .648-.291l1.86-2.171a.997.997 0 0 0-.085-1.39z',
                heading: 'call us',
                caption: '+1 (778) 886-0508',
              },
              {
                path: 'M20 4H4a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V6a2 2 0 0 0-2-2zm0 4.7-8 5.334L4 8.7V6.297l8 5.333 8-5.333V8.7z',
                heading: 'mail us',
                caption: 'info@teqoaccounting.com',
              }
            ],
            AccordionData: [
              {
                item1: 'it helps plan for growth',
                item2: 'to attract investors',
                item3: 'to gets you paid',
                item4: 'accounting keeps you on top of debts',
                item5: 'pay the right amount of taxes',
              }
            ]
        }
    },
    setup() {
        const onSwiper = (swiper) => {
            console.log(swiper);
        };
        const onSlideChange = () => {
            console.log('slide change');
        };
        
        return {
            onSwiper,
            onSlideChange,

        };
    },
 
}

</script>
<style>

/* index css */
.main-banner {
    padding-top: 198px;
}
.about-us, #OurServices, .bus-support, .testimonial, .contact-us, .questions {
    padding-top: 150px;
    padding-bottom: 100px;
}
.main-banner .swipe-slider-wrapper .swiper-button-prev::after {
  color: var(--white);

}

.swipe-slider-wrapper{
    background-image: url('../assets/images/carousel-before.png');
    background-repeat: no-repeat;
    padding: 88px 0px;
}
.swiper-slider-right h2{
    font-size: 60px;
    font-weight: 600;
    color: var(--tq-blue);
    margin-bottom: 15px;
}
.swiper-slider-right p{
    font-weight: 600;
    font-size: 18px;
    color: var(--tq-gray);
    margin-bottom: 30px;
}
.swiper-slider-right button{
    font-weight: 600;
    font-size: 18px;
    border:none;
    background-color: var(--tq-orange);
    color: var(--tq-white);
    padding: 6px 16px;
    border-radius: 33px;
}
/* index css end*/

/*color bar css */
 .color-bar {
    background-color: var(--tq-pinkish-white);
  }
  .inner-bar {
    height:100px;
    background-color: var(--tq-blue);
    width: 40%;
    clip-path: polygon(0 0,100% 0,92% 100%,0 100%);
  }
/*color bar css */

/* about us css */
.about-us {
    position: relative;
}
.about-us::before{
    position: absolute;
    content: "";
    right: 0;
    top: 0;
    height: 100%;
    border-top: 500px solid var(--tq-orange);
    border-left: 470px solid transparent;
    opacity: .35;
    z-index: 0;
}
.about-us::after {
    position: absolute;
    content: "";
    right: 0;
    top: 0;
    height: 100%;
    border-bottom: 500px solid var(--tq-orange);
    border-left: 470px solid transparent;
    opacity: .35;
    z-index: 0;
}
.about-content h4{
    font-weight: 500;
    font-size: 19px;
    color: var(--tq-orange);
}
.about-content h3{
    font-size: 30px;
    color: var(--tq-blue);
    font-weight: 600;
    margin-bottom: 20px;
}
.about-content p {
    line-height: 35px;
    font-size: 18px;
}
.about-image-three {
  margin-top: 13px;
}
.about-image-show {
  height: fit-content;
  display: flex;
  align-items: end;
}
.about-us-icon {
  background: var(--tq-blue);
  height: 180px;
  width: 180px;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 2;
}
.about-us-icon h3{
  border: 1px dashed var(--tq-orange);
  border-radius: 50%;
  height: 140px;
  width: 140px;
  display: grid;
  place-items: center;
  margin: 0;
}
/* about us css */

/* Our Services css */
#OurServices {
  background-color: var(--tq-pinkish-white);
}
/* Our Services css */

/* Accounting css */
.accounting-section {
    padding-top: 150px;
}
.services-item {
    background-color: var(--tq-orange);
    padding: 37px;
    width: 95%;
    border-radius: 25px;
    overflow: hidden;
    margin-inline: auto;
    min-height: 377px !important;
}
.services-item h3 {
    font-weight: 700;
    font-size: 21px;
    color:var(--tq-white);
    margin-bottom: 20px;
}
.services-item p {
    color:var(--tq-white);
    margin-bottom: 1rem;
}
.services-item p img{
    width: 7%;
}
.image-services img{
    width: 48%;
}
.services-item::before {
    position: absolute;
    content: "";
    left: 0;
    top: 0;
    height: 100%;
    border-right: 240px solid transparent;
    opacity: .1;
    transition: all .5s ease;
    border-top: 240px solid var(--tq-white);
}
.services-item::after {
    position: absolute;
    content: "";
    left: 0;
    top: 0;
    height: 100%;
    border-right: 240px solid transparent;
    opacity: .1;
    transition: all .5s ease;
    border-bottom: 240px solid var(--tq-white);
}
/* Accounting css */

/* Taxation css */
.taxation-section {
  padding-top: 150px;
}
.item-active {
  background-color: var(--tq-pinkish-white);
  box-shadow: 1px 1px 10px var(--tq-taxation-shadow);
}
.item-active p{
  color: var(--white);
}
.item-active h3 {
  color: var(--tq-blue);
}
.item-active::before{
  border-top: 240px solid var(--tq-orange) ;
}
.item-active::after{
  border-bottom: 240px solid var(--tq-orange);
}
/* Taxation css */

/* advisory css */ 
.advisory-section {
  padding-top: 150px;
}
/* advisory css */ 

/* business support css */
.bus-support {
  position: relative;
  background-color: var(--tq-pinkish-white);
  background-image: url('../assets/images/work.jpg');
  background-repeat: no-repeat;
  background-size: cover;
}
.bus-support .container {
  position: relative;
  z-index: 1;
}
.bus-support::before {
  position: absolute;
  content: "";
  width: 100%;
  left: 0;
  height: 100%;
  top: 0;
  background-color: var(--tq-blue);
  opacity: .9;
}
.bus-support::after {
  position: absolute;
  content: "";
  width: 100%;
  left: 0;
  height: 65%;
  bottom: 0;
  background-color: var(--tq-pinkish-white);
  opacity: .9;
}
.business-description {
  color: var(--tq-white) !important;
}
.support-image img {
  width: 90%;
  border-radius: 30px;
}

.list-svg {
  height: 90px;
  width: 90px;
  background: var(--tq-bg-support);
  text-align: center;
  display: grid;
  place-items: center;
  border-radius: 5px;
}
.support-lists-row {
  background-color: var(--tq-white);
  padding: 20px 13px;
  margin-bottom: 20px;
}
.support-content h3 {
  font-size: 22px;
  font-weight: 600;
  color: var(--tq-blue);
}
.support-content p {
  line-height: 30px;
}
/* business support css */

/* Testimonial css  */

.testimonial-carousel {
  padding-top: 30px;
}

.all-testimonials p {
  font-size: 25px;
  font-weight: 600;
  text-align: justify;
  color: var(--tq-blue);
}
.client {
  padding-top: 30px;
}
.client p{
  color: var(--tq-blue);
  font-size: 20px;
  font-weight: 800;
  text-align: center;
}

/* Testimonial css  */

/* Useful links css*/
.useful-image img {
  width: 57%;
}
/* Useful links css*/

/* Contact Us css */

.find-us h2 {
  border-bottom: 2px solid var(--tq-red);
  padding-bottom: 10px;
}
.find-us h2 span {
  font-size: 27px;
  color: var(--tq-black);
  font-weight: 800;
}
.find-us {
  border: 2px solid var(--tq-red-pink);
  padding: 24px 16px;
  border-radius: 5px;
  border-top-left-radius: 52px;
  border-bottom-right-radius: 52px;
  margin: 20px auto;
}
.input-area input, .input-area textarea {
  width: 100%;
  background-color: var(--tq-form-background);
  border: unset;
  border-radius: 20px;
}
.input-area textarea {
  margin-bottom: 15px;
}
.input-area input {
  padding: 10px 20px;
  margin-bottom: 20px;
}
.input-area button {
  width: 100%;
  color: var(--tq-white);
  background-color: var(--tq-orange);
  border-radius: 32px;
  border: unset;
  padding: 10px;
  font-weight: 600;
}
/* Contact Us css */

/* faq css */
.questions {
  background-color: var(--tq-pinkish-white);
  position: relative;
}
.questions::before{
  position: absolute;
  content: "";
  right: 0;
  top: 0;
  height: 100%;
  border-top: 500px solid var(--tq-orange);
  border-left: 470px solid transparent;
  opacity: .35;
  z-index: 0;
}
.questions::after {
  position: absolute;
  content: "";
  right: 0;
  top: 0;
  height: 100%;
  border-bottom: 500px solid var(--tq-orange);
  border-left: 470px solid transparent;
  opacity: .35;
  z-index: 0;
}
.accordion-custom .accordion {
  border: unset;
}
.accordion-custom .accordion .accordion-item{
  box-shadow: var(--tq-box-shadow);
  margin: 20px auto;
}
.accordion-custom .accordion .accordion-item .accordion-header .accordion-button {
  background-color: var(--tq-pinkish-white);
  color: var(--tq-blue);
  font-weight: 600;
  box-shadow: unset;
  border: 1px solid var(--tq-pinkish-white);
  border-radius: 5px;
}
.accordion-custom .accordion .accordion-item .accordion-header .accordion-button:focus {
  outline: none;
  border-color: var(--tq-blue);
}
.accordion-custom .accordion .accordion-item .accordion-header .accordion-button:hover {
  border-color: var(--tq-blue);
}
.accordion-custom .accordion .accordion-item .accordion-header .accordion-button::after {
  background-image: url( "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='var(--tq-blue)' %3E%3Cpath d='M16.293 9.293 12 13.586 7.707 9.293l-1.414 1.414L12 16.414l5.707-5.707z'/%3E%3C/svg%3E" );
}
.accordion-custom .accordion .accordion-item .accordion-header .accordion-button:not(.collapsed)::after {
  background-image: url( "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='var(--tq-blue)' %3E%3Cpath d='M16.293 9.293 12 13.586 7.707 9.293l-1.414 1.414L12 16.414l5.707-5.707z'/%3E%3C/svg%3E" );
}
.accordion-inside p {
  line-height: 30px;
}
.accordion-inside ul li {
  list-style: none;
  color: var(--tq-black);
  font-size: 14px ;
  font-weight: 600;
  margin-bottom: 10px;
}
/* faq css */
.whatsapp {
  position: fixed;
  bottom: 30px;
  left: 30px;
  z-index: 1031 !important;
}
.whatsapp a {
  background-color: var(--tq-green);
  height: 60px;
  width: 60px;
  display: grid;
  place-items: center;
  border-radius: 50%;
  animation: pushOut 1.5s infinite;
}
/* media query */
@media all and (min-width: 1892px){
  .about-image-2 {
    width: 87%;
  }
}
@media all and (min-width: 320px) and (max-width: 1200px) {
    .accounting-section {
        padding-top: 50px;
    }
}
@media all and (min-width: 320px) and (max-width: 992px) {
    .swipe-slider-wrapper{
        background-image: unset;
        padding: 0;
    }
    .main-banner {
        padding-top: 120px;
    }
    .swipe-slider-wrapper{
        background-image: unset;
        padding: 0;
    }
    .main-banner {
        padding-top: 120px;
    }
     .about-content {
        text-align: center;
        margin-top: 30px;
    }
    .about-content h3 {
        font-size: 29px;
    }
    .about-content p {
        /* font-size: 15px; */
        line-height: 26px;
    }
    .about-us, #OurServices, .bus-support, .testimonial, .contact-us, .questions{
      padding: 50px 10px;
    }
    .services-description h3 {
      font-size: 25px;
    }
    .accounting-section, .taxation-section, .advisory-section, .testimonial-carousel {
      padding: 0;
    }
    .support-image img {
      width: auto;
    }
    .list-container {
      padding: 50px 10px 0px 10px;
    }
    .all-testimonials p {
      font-size: 18px;
    }
    .services-description  {
      margin-bottom: 0 !important;
    }
}
@media all and (min-width: 320px) and (max-width: 767px) {
    .swiper-slider-right {
        text-align: center;
    }
    .swiper-slider-right h2{
        font-size: 29px;
    }
    .swiper-slider-right p, .swiper-slider-right button{
        font-size: 15px;
    }
   
}
@media all and (min-width: 320px) and (max-width: 576px) {
    .image-services img{
        width: 70%;
    }
}

</style>
