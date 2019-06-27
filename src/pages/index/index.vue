<template>
  <div @click="clickHandle">
    <i-notice-bar icon="systemprompt" closable loop>
    新品上市！
    </i-notice-bar>
    <i-grid>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/milkyTea.png" @click="jump1"/>
        </i-grid-icon>
        <i-grid-label>至尊奶茶</i-grid-label>
    </i-grid-item>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/fruitTea.png" @click="jump2"/>
        </i-grid-icon>
        <i-grid-label>无敌果茶</i-grid-label>
    </i-grid-item>
    </i-grid>
    <i-grid>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/milkTea.png" @click="jump3"/>
        </i-grid-icon>
        <i-grid-label>鲜奶红茶</i-grid-label>
    </i-grid-item>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/tea.png" @click="jump4"/>
        </i-grid-icon>
        <i-grid-label>阿牧茗茶</i-grid-label>
    </i-grid-item>
    </i-grid>
    <i-grid>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/coffee.png" @click="jump5"/>
        </i-grid-icon>
        <i-grid-label>阿牧咖啡</i-grid-label>
    </i-grid-item>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/smoothies.png" @click="jump6"/>
        </i-grid-icon>
        <i-grid-label>阿牧冰沙</i-grid-label>
    </i-grid-item>
    </i-grid>
    <i-grid>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/juice.png" @click="jump7"/>
        </i-grid-icon>
        <i-grid-label>鲜榨果汁</i-grid-label>
    </i-grid-item>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/fruit.png" @click="jump8"/>
        </i-grid-icon>
        <i-grid-label>阿牧果粒多</i-grid-label>
    </i-grid-item>
    </i-grid>
    <i-grid>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/dessert.png" @click="jump9"/>
        </i-grid-icon>
        <i-grid-label>甜点</i-grid-label>
    </i-grid-item>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/snack.png" @click="jump10"/>
        </i-grid-icon>
        <i-grid-label>小吃</i-grid-label>
    </i-grid-item>
</i-grid>
  </div>
</template>

<script>
import card from '@/components/card'

export default {
  data () {
    return {
      motto: 'Hello miniprograme',
      userInfo: {
        nickName: 'mpvue',
        avatarUrl: 'http://mpvue.com/assets/logo.png'
      }
    }
  },

  components: {
    card
  },

  methods: {
    jump1(){
      wx.navigateTo({
        url: '/pages/naicha/main'
      })
    },
    jump2(){
      wx.navigateTo({
        url: '/pages/guocha/main'
      })
    },
    jump3(){
      wx.navigateTo({
        url: '/pages/hongcha/main'
      })
    },
    jump4(){
      wx.navigateTo({
        url: '/pages/mingcha/main'
      })
    },
     jump5(){
      wx.navigateTo({
        url: '/pages/coffe/main'
      })
    },
    jump6(){
      wx.navigateTo({
        url: '/pages/ice/main'
      })
    },
    jump7(){
      wx.navigateTo({
        url: '/pages/juice/main'
      })
    },
    jump8(){
      wx.navigateTo({
        url: '/pages/guoliduo/main'
      })
    },
     jump9(){
      wx.navigateTo({
        url: '/pages/sweetee/main'
      })
    },
    jump10(){
      wx.navigateTo({
        url: '/pages/fingerfood/main'
      })
    },
  },
}
</script>

<style scoped>
.userinfo {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.userinfo-avatar {
  width: 128rpx;
  height: 128rpx;
  margin: 20rpx;
  border-radius: 50%;
}

.userinfo-nickname {
  color: #aaa;
}

.usermotto {
  margin-top: 150px;
}

.form-control {
  display: block;
  padding: 0 12px;
  margin-bottom: 5px;
  border: 1px solid #ccc;
}
.all{
  width:7.5rem;
  height:1rem;
  background-color:blue;
}
.all:after{
  display:block;
  content:'';
  clear:both;
}
.left{
  float:left;
  width:3rem;
  height:1rem;
  background-color:red;
}

.right{
  float:left;
  width:4.5rem;
  height:1rem;
  background-color:green;
}
</style>
