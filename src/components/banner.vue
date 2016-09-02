<template>
    <section class="banner">
        <div class="swiper-container">
          <div class="swiper-wrapper">
            <a class="swiper-slide" :style="{'background-image': 'url(' + s + ')'}" v-for="s in srcs" :href="hrefs[$index]"></a>
          </div>
          <div class="swiper-pagination swiper-pagination-clickable swiper-pagination-bullets"><span class="swiper-pagination-bullet swiper-pagination-bullet-active"></span><span class="swiper-pagination-bullet"></span><span class="swiper-pagination-bullet"></span><span class="swiper-pagination-bullet"></span><span class="swiper-pagination-bullet"></span><span class="swiper-pagination-bullet"></span><span class="swiper-pagination-bullet"></span><span class="swiper-pagination-bullet"></span><span class="swiper-pagination-bullet"></span><span class="swiper-pagination-bullet"></span></div>
        </div>
    </section>

    <!--<script src="http://ac-tarzdewf.clouddn.com/bc97396fb1126268.js"></script>-->
</template>
<style lang="scss" scope>
    .banner .swiper-container {
      height: 3.8125rem;
        .swiper-wrapper {
            .swiper-slide {
              -webkit-background-size: cover;
              background-size: cover;
              background-position: 100% 50%;
            }
        }

      .swiper-pagination {
        bottom: 5px;

        .swiper-pagination-bullet{
          background-color: #ffffff;
          opacity: .5;
          width: 10px;
          height: 10px;
          &.swiper-pagination-bullet-active {
            background-color: #ff5200;
            opacity: 1;
          }
        }
      }


    }
</style>
<script>
    import Swiper from 'swiper'
    import Vue from 'vue'
    Vue.component('banner',{
        template: '<section class="banner">\
                      <div class="swiper-container banner-swiper">\
                        <div class="swiper-wrapper">\
                          <a class="swiper-slide" :style="{\'background-image\': \'url(\' + s + \')\'}" v-for="s in srcs" :href="hrefs[$index]"></a>\
                        </div>\
                        <div class="banner-pagination swiper-pagination swiper-pagination-clickable swiper-pagination-bullets"></div>\
                      </div>\
                  </section>',
        props: ['srcs', 'hrefs'],
        data(){
            return{
                msg:'hello vue'
            }
        },
        ready: function () {
            var mySwiper = new Swiper('.banner-swiper', {
                autoplay: 3000,//可选选项，自动滑动
              // 如果需要分页器
              pagination: '.banner-pagination',
            })
            console.log('banner ready')
        },
        components:{
        }
    })
</script>
