<template>
  <li class="goods">
    <h1 class="itemName">{{goodsname}}</h1>
    <h4 class="itemDetail">{{detail}}</h4>
    <div class="salesale">
      <h4 class='orange itemNum'>{{num}}</h4>
      <h4 class="intergralFont">&nbsp;&nbsp;&nbsp;积分</h4>
    </div>
    <img :src="pic" alt="" class="itemPic"/>
    <a type="button" class="btn-orange btn-exchange" name="byButton">{{num}}分兑</a>
  </li>
</template>

<script>
import Vue from 'vue'

Vue.component('goods',{
    template: '<li class="goods">\
                <h1 class="itemName">{{goodsname}}</h1>\
                <h4 class="itemDetail">{{detail}}</h4>\
                <div class="sale">\
                  <h4 class="orange itemNum">{{num}}</h4>\
                  <h4 class="intergralFont">&nbsp;&nbsp;&nbsp;积分</h4>\
                </div>\
                <img :src="pic" alt="" class="itemPic"/>\
                <button type="button" class="btn-orange btn-exchange" name="byButton">{{num}}分兑</button>\
                </li>',
    props: ['goodsname','detail','integral','pic','num'],
    data () {
      return {
        // name:'产品名产品名',
        // detail:'注:产品介绍,讲解注释与标识讲解方法,作用',
        // integral:'20000',
        // pic:'http://ac-a8f3kcal.clouddn.com/80c16c57623bd584.png',
        // num:'2000'
      }
    }
})
</script>
<style lang='scss' scope>
  .goods {
    background-color: #fff;
    padding: .25rem .25rem .125rem .1875rem;
    position: relative;
    .itemName , .sale , .itemDetail  {
      line-height: .45rem;
    }
    .itemDetail {
      overflow: hidden;
      text-overflow: ellipsis;
      white-space: nowrap;
      padding-right: 10px;
    }

    .sale, .itemDetail, .itemName {
      padding-left: .1rem;
    }
    .sale {
      display: flex;
      line-height: .6rem;
    }
    .itemPic {
      width: 92%;
      height: 2.3rem;
      margin-top: .05rem;
      margin-bottom: .15rem;
      /*background-color: #345678;*/
    }
    .btn-exchange {
      position: absolute;
      right: .5rem;
      bottom: .25rem;
      padding: .15rem .3rem;
      display: block;
    }
  }
</style>
