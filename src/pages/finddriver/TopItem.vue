<template>
  <a class="topItem" href="../workdetail/index.html">
    <div class="line1">
      <img class="money" src="./img/money.png" alt="">
      <span class="number">月薪：{{topObj.salary}}元/月</span>
      <tag v-for="(item, index) in topObj.tagList" :key="index" :tagName='item.name'></tag>
    </div>
    <div class="line2">
      <span>地点：{{topObj.address}}</span>
    </div>
    <img class="jipin" src="./img/jipin.png" alt="">
  </a>  
</template>

<script>
import Tag from '@/components/Tag.vue'
export default {
  props:{
    topObj: Object
  },
  components:{
    Tag
  }
}
</script>

<style lang='less' scoped>
  .topItem{
    display: block;
    background-color: #fffcf8;
    position: relative;
    padding-left: 0.24rem;
    font-size: 0.24rem;
    border-top: 1px solid #bfbfbf;
    img{
      vertical-align: middle;
    }
    .line1{
      height: 0.53rem;
      line-height: 0.53rem;
      border-bottom: 1px solid #e4e4e4;
      .money{
        width: 0.30rem;
        margin-right: 0.1rem;
      }
      .number{
        margin-right: 0.2rem;
        color: @theme-color;
      }
    }
    .line2{
      height: 0.62rem;
      line-height: 0.62rem;
      span{
        color: @second-color;
      }
    }
    .jipin{
      position: absolute;
      display: block;
      right: 0.2rem;
      top: 0;
      width: 0.48rem;
    } 
  }
</style>
