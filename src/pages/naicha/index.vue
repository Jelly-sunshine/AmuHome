
<template>
  <div>
     <div class="blank"></div>
    <i-card v-for="item in action" :key="item" :title="item.carNum" :extra="'价格：'+item.price">
        <view slot="content">温度：{{item.temperature}}
          <i-button i-class="re_button" @click="handleClick(item,index)" type="info" size="small">点击预约</i-button>
        </view>
        <view slot="footer">甜度：{{item.sweet}}</view>
    </i-card>
    </div>

   

</template>

<script>
  

  export default {
   
    data() {
      return {
        userInfo: {
          price:'',
          temperature:'',
          sweet:''
        }
      }
    }
  }

</script>

<style>
  .blank{
    display:block;
    width:100%;
    height:10px;
}
</style>

