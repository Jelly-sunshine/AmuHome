<template>
  <div>
    <view class="top-padding">
    <view v-for="item in commdity" :key='item' class="top-padding">
    <i-card title="item.name" extra="item.price" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
    <view slot="content">{{item.remark}}</view>
    <view slot="footer">尾部内容</view>
    </i-card>
    </view>
    </view>
  </div>
</template>

<script>
import card from '@/components/card'

export default {
  components: {
    card
  },

  data () {
    return {
      commodity: []
    }
  },

  created () {
    const db = wx.cloud.database({ env: 'amuhome-0c79b8' })
    db.collection('commodity').get().then(
      res => {
        console.log(res.data)
        this.commodity = res.data
      }
    )
  }
}
</script>

<style>
.log-list {
  display: flex;
  flex-direction: column;
  padding: 40rpx;
}

.log-item {
  margin: 10rpx;
}
</style>
