<template>
  <div @click="clickHandle">
    <i-notice-bar icon="systemprompt" closable loop>
    新品上市！
    </i-notice-bar>
    <i-grid>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/milkyTea.png" />
        </i-grid-icon>
        <i-grid-label>至尊奶茶</i-grid-label>
    </i-grid-item>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/fruitTea.png" />
        </i-grid-icon>
        <i-grid-label>无敌果茶</i-grid-label>
    </i-grid-item>
    </i-grid>
    <i-grid>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/milkTea.png" />
        </i-grid-icon>
        <i-grid-label>鲜奶红茶</i-grid-label>
    </i-grid-item>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/tea.png" />
        </i-grid-icon>
        <i-grid-label>阿牧茗茶</i-grid-label>
    </i-grid-item>
    </i-grid>
    <i-grid>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/coffee.png" />
        </i-grid-icon>
        <i-grid-label>阿牧咖啡</i-grid-label>
    </i-grid-item>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/smoothies.png" />
        </i-grid-icon>
        <i-grid-label>阿牧冰沙</i-grid-label>
    </i-grid-item>
    </i-grid>
    <i-grid>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/juice.png" />
        </i-grid-icon>
        <i-grid-label>鲜榨果汁</i-grid-label>
    </i-grid-item>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/fruit.png" />
        </i-grid-icon>
        <i-grid-label>阿牧果粒多</i-grid-label>
    </i-grid-item>
    </i-grid>
    <i-grid>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/dessert.png" />
        </i-grid-icon>
        <i-grid-label>甜点</i-grid-label>
    </i-grid-item>
    <i-grid-item>
        <i-grid-icon>
            <image src="/static/images/snack.png" />
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
    bindViewTap () {
      const url = '../logs/main'
      if (mpvuePlatform === 'wx') {
        mpvue.switchTab({ url })
      } else {
        mpvue.navigateTo({ url })
      }
    },
    clickHandle (ev) {
      console.log('clickHandle:', ev)
      // throw {message: 'custom test'}
    }
  },

  created () {
    // let app = getApp()
  }
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
