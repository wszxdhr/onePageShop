<template>
  <div id="app">
    <banner id="banner" class="section" :srcs="banner.srcs" :hrefs="banner.hrefs"></banner>
    <homeinfo id="home-info" class="section" :integral="homeInfo.integral" :lefthref="homeInfo.leftHref" :btnhref="homeInfo.btnHref" :lefttext="homeInfo.leftText"></homeinfo>
    <homenav></homenav>
    <prizelist :list="prizeList"></prizelist>
    <goodlist :list="goodList" :goodbar="goodBar"></goodlist>

  </div>
</template>

<script>
import Goods from './components/goods'
import Banner from './components/banner'
import Homeinfo from './components/homeInfo'
import Homenav from './components/homeNav'
import Goodlist from './components/goodlist'
import Prizelist from './components/prizelist'

export default {
  components: {
    Goods,Banner,Homeinfo,Homenav,Goodlist,Prizelist
  },
  data() {
    return {
      homeInfo: {
        integral: '1000',
        leftHref: 'http://www.baidu.com',
        btnHref: 'http://www.sohu.com',
        leftText: '如何获得更多积分?'
      },
      banner: {
        srcs: [
          'https://ss2.bdstatic.com/8_V1bjqh_Q23odCf/pacific/735790408.jpg',
          'https://t10.baidu.com/it/u=441978915,3319695905&fm=76',
          'https://ubmcmm.baidustatic.com/media/v1/0f000AgtA7FS-x4ZVf_sA0.jpg',
          'https://t10.baidu.com/it/u=1779003342,2627210414&fm=76'
        ],
        hrefs: [
          'http://www.baidu.com',
          'http://www.sohu.com',
          'http://www.sina.com',
          'http://www.google.com',
        ]
      },
      prizeList: [
        'flexflexflexflexflexflexflexflexflexflexflex',
        'webkitwebkitwebkitwebkitwebkitwebkitwebkitwebkitwebkit',
        'sbsbsbsbsbsbsbsbsbsbsbsbsbsbsbsbsbsbsbsbsbsbsbsbsbsbsb'
      ],
      goodBar: [
        '推荐出装','0元购','折扣','花钱呗'
      ],
      goodList: [
        {
          name:'产品名产品名',
          detail:'注:产品介绍,讲解注释与标识讲解方法,作用',
          integral:'20000',
          pic:'https://ss3.baidu.com/9fo3dSag_xI4khGko9WTAnF6hhy/vip/whcrop%3D176%2C106/sign=1b7f049a66061d957d13617a148437e0/8326cffc1e178a820b7f0202fe03738da877e8d5.jpg',
          num:'2000',
          picHref: 'http://www.baidu.com',
          clickHref: 'http://www.sohu.com',
          btnHref: 'http://www.cctv.com'
        },
        {
          name:'产品名产品名',
          detail:'注:产品介绍,讲解注释与标识讲解方法,作用',
          integral:'20000',
          pic:'https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=2437161509,401295148&fm=80',
          num:'2000',
          picHref: 'http://www.baidu.com',
          clickHref: 'http://www.sohu.com',
          btnHref: 'http://www.cctv.com'
        },
        {
          name:'产品名产品名',
          detail:'注:产品介绍,讲解注释与标识讲解方法,作用',
          integral:'20000',
          pic:'https://ss1.baidu.com/6ONXsjip0QIZ8tyhnq/it/u=2476270816,1666316684&fm=80',
          num:'2000',
          picHref: 'http://www.baidu.com',
          clickHref: 'http://www.sohu.com',
          btnHref: 'http://www.cctv.com'
        },
        {
          name:'产品名产品名',
          detail:'注:产品介绍,讲解注释与标识讲解方法,作用',
          integral:'20000',
          pic:'https://ss0.baidu.com/6ONWsjip0QIZ8tyhnq/it/u=2218513521,3784381242&fm=80',
          num:'2000',
          picHref: 'http://www.baidu.com',
          clickHref: 'http://www.sohu.com',
          btnHref: 'http://www.cctv.com'
        },
        {
          name:'产品名产品名',
          detail:'注:产品介绍,讲解注释与标识讲解方法,作用',
          integral:'20000',
          pic:'http://ac-a8f3kcal.clouddn.com/80c16c57623bd584.png',
          num:'2000',
          picHref: 'http://www.baidu.com',
          clickHref: 'http://www.sohu.com',
          btnHref: 'http://www.cctv.com'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
  #app {
    width: 100%;
  }
  html {
    &,body{
      width: 100%;
      height: 100%;
      margin: 0;
      padding: 0;
      display: flex;
      flex-wrap: wrap;
    }
  }
</style>
