<template>
<div class="setting-form">
  <div class="setting-border border-horizontal"></div>
  <div class="setting-border border-horizontal"></div>
  <div class="setting-border border-vertical"></div>
  <div class="setting-border border-vertical"></div>
  <div class="setting-item" v-for="(item, index) in items">
    <p>{{ item.title }}</p>
    <img src="../../../../assets/pages/UserSetting/btn_r.png" />
    <span>{{ item.text }}</span>
    <div v-if="index < (items.length - 1)"></div>
  </div>
</div>
</template>

<script>
export default {
  props: [ 'items' ]
}
</script>

<style>
.setting-form {
  position: relative;
  width: 100%;
  border: 0;
  height: auto
}
.setting-border {
  position: absolute;
  border: 1px solid #8a683a;
}
.border-horizontal {
  width: 1vw;
  height: 100%;
}
.border-horizontal:nth-child(1) {
  left: -1vw;
  border-right: 0;
}
.border-horizontal:nth-child(2) {
  right: -1vw;
  border-left: 0;
}
.border-vertical {
  width: 100%;
  height: 1vw;
}
.border-vertical:nth-child(3) {
  top: -1vw;
  border-bottom: 0;
}
.border-vertical:nth-child(4) {
  bottom: -1vw;
  border-top: 0;
}
.setting-item {
  position: relative;
  width: 100%;
  height: 8vw;
  line-height: 8vw;
  padding: 0 3%;
  font-size: 5vw;
  cursor: pointer;
}
.setting-item > p {
  margin: 0;
  float: left;
  text-align: center;
  color: #8b6d63
}
.setting-item > img {
  float: right;
  width: 5%;
  height: 80%;
  //top: 50%;
  transform: translate(0, 12%);
  margin-left: 2%;
}
.setting-item > span {
  float: right;
  color: #5d5749;
  font-size: 4.5vw;
}
.setting-item > div {
  width: calc(100% + 6vw);
  height: 100%;
  position: relative;
  left: -3vw;
  border-bottom: 1px solid #927c74;
}
</style>