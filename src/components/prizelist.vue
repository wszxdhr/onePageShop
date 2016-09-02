<template>
    <section id="prize-list">
      <h2 class="prize-title">中奖快报: </h2> <h2 class="prize-info" v-show="showPrize" transition="fade">{{list[current%list.length]}}</h2>
    </section>
</template>
<style lang="scss">
  #prize-list {
    display: flex;
    display: -webkit-flex;
    padding: .3125rem .375rem .3125rem .375rem;
    border-top: 1px solid #d9d9d9;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
    .prize-title {
      margin-right: 10px;
    }

    .prize-info {
      text-align: center;
      flex: 1;
      -webkit-flex: 1;
    }
  }
</style>
<script>
    import Vue from 'vue'
    Vue.component('prizelist',{
        template: '<section id="prize-list"><h2 class="prize-title">中奖快报: </h2> <h2 class="prize-info" v-show="showPrize" transition="fade">{{list[current%list.length]}}</h2></section>',
        props: ['list'],
        data(){
            return{
                current: 0,
                showPrize: true
            }
        },
        ready: function () {
            var that = this;
            setInterval(function(){
                that.showPrize = false
                setTimeout(function(){
                  that.showPrize = true
                  that.current++
                },300);
            },3000);
        },
        components:{
        }
    })
</script>
