<template>
  <div id="index" class="main-banner">
    <swiper
        :slides-per-view="1"
        :space-between="50"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
        :autoplay="{delay:2000, disableOnInteraction: false,}"
        :navigation="true"
        :modules="modules"
        :loop="true"
        :pagination="{clickable: true,}"
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
            <div class="col-12 col-md-5">
right
            </div>
            <!-- col-12 col-md-5 -->
            <div class="col-12 col-md-5">
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
              <div class="col-12 col-md-12 col-lg-5 col-xl-4">
                  <div class="accounting-content">
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
              <div class="col-12 col-md-12 col-lg-7 col-xl-7">
                  <div class="image-services text-center mt-5 mt-xl-0">
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
              <div class="col-12 col-md-12 col-lg-5 col-xl-4">
                  <div class="accounting-content">
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
              <div class="col-12 col-md-12 col-lg-7 col-xl-7">
                  <div class="image-services text-center mt-5 mt-xl-0">
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
            <div class="support-image">
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
                                      <svg class="mb-3" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="60" height="60" style="fill: var(--tq-orange);"><path d="m21.95 8.721-.025-.168-.026.006A4.5 4.5 0 1 0 17.5 14c.223 0 .437-.034.65-.065-.069.232-.14.468-.254.68-.114.308-.292.575-.469.844-.148.291-.409.488-.601.737-.201.242-.475.403-.692.604-.213.21-.492.315-.714.463-.232.133-.434.28-.65.35l-.539.222-.474.197.484 1.939.597-.144c.191-.048.424-.104.689-.171.271-.05.56-.187.882-.312.317-.143.686-.238 1.028-.467.344-.218.741-.4 1.091-.692.339-.301.748-.562 1.05-.944.33-.358.656-.734.909-1.162.293-.408.492-.856.702-1.299.19-.443.343-.896.468-1.336.237-.882.343-1.72.384-2.437.034-.718.014-1.315-.028-1.747a7.028 7.028 0 0 0-.063-.539zm-11 0-.025-.168-.026.006A4.5 4.5 0 1 0 6.5 14c.223 0 .437-.034.65-.065-.069.232-.14.468-.254.68-.114.308-.292.575-.469.844-.148.291-.409.488-.601.737-.201.242-.475.403-.692.604-.213.21-.492.315-.714.463-.232.133-.434.28-.65.35l-.539.222c-.301.123-.473.195-.473.195l.484 1.939.597-.144c.191-.048.424-.104.689-.171.271-.05.56-.187.882-.312.317-.143.686-.238 1.028-.467.344-.218.741-.4 1.091-.692.339-.301.748-.562 1.05-.944.33-.358.656-.734.909-1.162.293-.408.492-.856.702-1.299.19-.443.343-.896.468-1.336.237-.882.343-1.72.384-2.437.034-.718.014-1.315-.028-1.747a7.571 7.571 0 0 0-.064-.537z"></path></svg>
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
                        <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-orange);transform: ;msFilter:;"><path d="M20 6c0-2.168-3.663-4-8-4S4 3.832 4 6v2c0 2.168 3.663 4 8 4s8-1.832 8-4V6zm-8 13c-4.337 0-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3c0 2.168-3.663 4-8 4z"></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.firstPara }}</p>
                        <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-orange);transform: ;msFilter:;"><path d="M20 6c0-2.168-3.663-4-8-4S4 3.832 4 6v2c0 2.168 3.663 4 8 4s8-1.832 8-4V6zm-8 13c-4.337 0-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3c0 2.168-3.663 4-8 4z"></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.secondPara }}</p>
                        <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-orange);transform: ;msFilter:;"><path d="M20 6c0-2.168-3.663-4-8-4S4 3.832 4 6v2c0 2.168 3.663 4 8 4s8-1.832 8-4V6zm-8 13c-4.337 0-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3c0 2.168-3.663 4-8 4z"></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.thirdPara }}</p>
                        <p><svg class="mb-1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" style="fill: var(--tq-orange);transform: ;msFilter:;"><path d="M20 6c0-2.168-3.663-4-8-4S4 3.832 4 6v2c0 2.168 3.663 4 8 4s8-1.832 8-4V6zm-8 13c-4.337 0-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3c0 2.168-3.663 4-8 4z"></path><path d="M20 10c0 2.168-3.663 4-8 4s-8-1.832-8-4v3c0 2.168 3.663 4 8 4s8-1.832 8-4v-3z"></path></svg>&nbsp;{{ data.fourthPara }}</p>
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
      
    </div>
</div>
<!-- contact-us -->
</template>

<script>
// @ is an alias to /src
// Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from "swiper/vue";
  import 'swiper/css';
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
              },
              {
                content: "In this expensive world, every business owner is looking for smart and budgeted book-keeping solutions. Hiring a team of accountants can be expensive for business. That's why I choose Teqo accounting software. It’s an ai accounting tool that allows business owners to manage expenses, pay bills or collect receipts under one roof.",
                client: 'John',
              },
              {
                content: "I am very pleased to tell you about one of excellent accounting software, Teqo accounting. Now, you don’t need to find accounting books to see previous records. You can get quick access to track your estimation progress. This software allows sending automatic reports on a specific set of times- quarterly, weekly, monthly, etc.",
                client: 'Dawayne',
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
    methods: {
         
    }
}

</script>
<style>

/* index css */
.main-banner {
    padding-top: 198px;
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
      padding-top: 150px;
      padding-bottom: 100px;
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
/* about us css */

/* Our Services css */
#OurServices {
  background-color: var(--tq-pinkish-white);
  padding-top: 150px;
  padding-bottom: 100px;
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
  padding-top: 150px;
  padding-bottom: 100px;
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

.testimonial {
  padding-top: 150px;
  padding-bottom: 100px;
}
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
/* media query */
@media all and (max-width: 1200px) {
    .accounting-section {
        padding-top: 50px;
    }
}
@media all and (max-width: 992px) {
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
}
@media all and (max-width: 767px) {
    .swiper-slider-right {
        text-align: center;
    }
    .swiper-slider-right h2{
        font-size: 29px;
    }
    .swiper-slider-right p, .swiper-slider-right button{
        font-size: 15px;
    }
    .about-content {
        text-align: center;
    }
    .about-content h3 {
        font-size: 29px;
    }
    .about-content p {
        font-size: 15px;
        line-height: 26px;
    }
}
@media all and (max-width: 576px) {
    .image-services img{
        width: 70%;
    }
}

</style>
