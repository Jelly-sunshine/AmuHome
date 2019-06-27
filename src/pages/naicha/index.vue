
<template>
  <div>
     <div class="blank"></div>
      <i-card i-class="re_card" v-for="item in action" :key="item" :title="item.name" :extra="item.price" :thumb="item.image">
        <view slot="content">温度：{{item.temperature}}
        </view>
        <view slot="footer">甜度：{{item.sweet}}</view>
      </i-card>
    </div>

   

</template>

<script>
  

  export default {
   
    data() {
      return {
          name:'',
          price:'',
          temperature:'',
          sweet:'',
          image:'',
          action:[{
            name:'奶茶1',
            price:'38元一杯',
            temperature:'20°',
            sweet:'高糖',
            image:'/static/images/milkTea.png'
          },{
            name:'奶茶2',
            price:'26元一杯',
            temperature:'23°',
            sweet:'低糖',
            image:'/static/images/fruit.png'
          }]
        }
    }
  }

</script>

<style scoped>
  div >>> .re_card{
    margin-top:5px;
  }
  .blank{
    display:block;
    width:100%;
    height:10px;
}
</style>

