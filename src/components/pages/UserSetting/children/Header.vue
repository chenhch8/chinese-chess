<template>
<div id="setting-header">
  <div id="setting-back"
       @click="goBack()"
       @mouseup="changeState(false)"
       @mousedown="changeState(true)">
    <img :src="img.back_btn" v-if="!isClick" />
    <img :src="img.back_btn_press" v-if="isClick" />
  </div>
  <div id="setting-header-user"
       class="background-container"
       :style="{ backgroundImage: 'url(' + img.userbg + ')' }">
    <div id="setting-header-user-portrait">
       <img :src="img.usr" v-if="img.usr" />
    </div>
    <p>{{ usrAccount }}</p>
  </div>
</div>
</template>

<script>
export default {
  props: [ 'usrType', 'usrAccount' ],
  data() {
    return {
      img: {
        userbg: require('@/assets/pages/UserSetting/header-user.png'),
        back_btn_press: require('@/assets/pages/UserSetting/back_btn_press.png'),
        back_btn: require('@/assets/pages/UserSetting/back_btn.png'),
        usr: null
      },
      isClick: false
    }
  },
  created: function() {
    switch(this.usrType) {
      case 1:
        this.img.usr = require('@/assets/portraits/man_head01.png');
        break;
      case 2:
        this.img.usr = require('@/assets/portraits/man_head02.png');
        break;
      case 3:
        this.img.usr = require('@/assets/portraits/women_head01.png');
        break;
      case 4:
        this.img.usr = require('@/assets/portraits/women_head02.png');
        break;
      default:
        this.img.usr = require('@/assets/portraits/default_head.png');
    }
  },
  methods: {
    // TODO
    goBack() {
      console.log('返回主页')
    },
    changeState(state) {
      this.isClick = state
    }
  }
}
</script>

<style>
#setting-header {
  position: relative;
  width: 100%;
  height: 18vh;
}
#setting-header-user {
  height: 18vh; width: 18vh;
  position: absolute;
  left: 50%;
  transform: translate(-50%, 0);
  background: no-repeat;
  background-size: 100% 100%
}
#setting-back {
  position: absolute;
  height: 6vh; width: 6vh;
  border-radius: 100%;
  left: 2vw; top: 2vw;
  cursor: pointer;
}
#setting-back > img {
  height: 100%; width: 100%;
}
#setting-header-user-portrait {
  position: absolute;
  width: 55%; height: 55%;
  left: 50%; top: 5%;
  border-radius: 100%;
  transform: translate(-50%, 0);
  background-color: #d0b399
}
#setting-header-user-portrait > img {
  position: absolute;
  width: 90%; height: 90%;
  border-radius: 100%;
  left: 50%; top: 50%;
  transform: translate(-50%, -50%);
}
#setting-header-user > p {
  position: relative;
  height: 25%;
  color: #d0b399;
  margin: 0;
  text-align: center;
  top: 63%;
}
</style>