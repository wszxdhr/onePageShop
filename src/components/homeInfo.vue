<template>
  <section class="home-info">
    <a class="left-box">
      <h1>我的积分<span class="orange h1">{{integral}}</span></h1>
      <h3 class="detail">{{leftText}}</h3>
    </a>
    <div class="btn-box">
      <a class="btn-default h2">兑换记录</a>
    </div>

  </section>
</template>
<style lang="scss" scope>
  .home-info {
    display: flex;
    padding: .3125rem .25rem .3125rem .25rem;

    .left-box {
      display: block;
      flex: 1;
      h1 {
        display: flex;
      }

      .detail {
        line-height: 1.5;
      }
    }

    .btn-box {
      padding-left: 20px;
      .btn-default {
        width: 1.7rem;
        height: .8rem;
        display: block;
        line-height: .8rem;
        text-align: center;
      }
    }
  }
</style>
<script>
  import Vue from 'vue'

  Vue.component('homeinfo', {
    template: '<section class="home-info"><a class="left-box" :href="lefthref"><h1>我的积分<span class="orange h1">{{integral}}</span></h1><h3 class="detail">{{lefttext}}</h3></a><div class="btn-box"><a class="btn-default h2" :href="btnhref">兑换记录</a></div></section>',
    props: ['integral','lefthref','btnhref','lefttext'],
    data () {
      return{

      }
    },
    components: {
    }
  })
</script>



/** WEBPACK FOOTER **
** homeInfo.vue?50fc13e8
**/
