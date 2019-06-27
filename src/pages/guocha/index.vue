
<template>
  <div>
      <view class="userinfo">
      <view class="userinfo-avatar">
      <open-data type="userAvatarUrl"></open-data>
      </view>
      <open-data class="userinfo-nickname" type="userNickName"></open-data>
      </view>

      <i-cell-group>
          <i-cell title="登录" is-link url="/pages/login/main"></i-cell>
          <i-cell title="我的订单" is-link url="/pages/map/main"></i-cell>
      </i-cell-group>
    </div>

   

</template>

<script>
  

  export default {
   
    data() {
      return {
        userInfo: {
        nickName: 'mpvue',
        avatarUrl: 'http://mpvue.com/assets/logo.png'
        }
      }
    }
  }

</script>

<style>
  .userinfo {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #f76a24;
  }

  .userinfo-avatar {
    width: 128rpx;
    height: 128rpx;
    margin-top: 10rpx;
    border-radius: 50%;
    clip-path: circle(64rpx at center);
  }

  .userinfo-nickname {
    color: #fff;
    padding: 5px;
  }
</style>

