<template>
    <ul class="goodbar">
      <goodbartab></goodbartab>

    </ul>

    <section class="good-list">
      <goods :goodsname="'adasdf'" :detail="'adsfadfalksdfjalksdjfa'" :integral="1000" :pic="" :num="213123" v-for="g in 9"></goods>
    </section>
</template>
<style lang="scss">
  .goodbar {
    display: flex;
    display: -webkit-flex;
    border-top: 1px solid #d9d9d9;
    border-bottom: .0725rem solid #d9d9d9;
    position: relative;

    .good-bar-tab {
      flex: 1;
      -webkit-flex: 1;
      text-align: center;
      font-weight: 500;
      line-height: 2.666666666;
    }
  }

  .good-list {
    width: 100%;
    display: flex;
    display: -webkit-flex;
    flex-wrap: wrap;
    .goods:nth-child(2n+1) {
      border-right: 1px solid #d9d9d9;
    }
    .goods {
      width: 50%;
      border-bottom: 1px solid #d9d9d9;
      // flex: 1;
      // background-color: #000;
    }
  }
</style>
<script>
  import Vue from 'vue'
  import Goods from './goods'
  Vue.component('goodlist',{
    template: '<ul class="goodbar"><goodbartab :title="title" v-for="title in goodbar"></goodbartab></ul><section class="good-list"><goods :goodsname="g.name" :detail="g.detail" :integral="g.integral" :pic="g.pic" :num="g.num" v-for="g in list"></goods></section>',
//    template: '<section id="prize-list"><h2 class="prize-title">中奖快报: </h2> <h2 class="prize-info" v-show="showPrize" transition="fade">{{list[current%list.length]}}</h2></section>',
    props: ['list','goodbar'],
    data(){
      return{
//        ]
      }
    },
    ready: function () {
    },
    components:{
      Goods,
      Goodbartab: {
        template: '<li class="good-bar-tab h1">{{title}}</li>',
        props: ['title']
      }
    }
  })
</script>
