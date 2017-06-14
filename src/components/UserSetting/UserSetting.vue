<template>
<div id="user-setting">

  <mu-row gutter>
    <mobile-tear-sheet>
      <mu-list>
        <mu-list-item :title="user.name" :describeText="user.description">
          <mu-avatar slot="leftAvatar" :src="user.avatar"></mu-avatar>
        </mu-list-item>
      </mu-list>
    </mobile-tear-sheet>
  </mu-row>

  <mu-row gutter>
    <mobile-tear-sheet>
      <mu-list>
        <mu-list-item :title="user.name" :describeText="user.description">
          <mu-avatar slot="leftAvatar" :src="user.avatar"></mu-avatar>
        </mu-list-item>
      </mu-list>
    </mobile-tear-sheet>
  </mu-row>

  <mu-row gutter>
    <mobile-tear-sheet>
      <mu-list>
        <mu-list-item :title="user.name" :describeText="user.description">
          <mu-avatar slot="leftAvatar" :src="user.avatar"></mu-avatar>
        </mu-list-item>
      </mu-list>
    </mobile-tear-sheet>
  </mu-row>

</div>
</template>

<script>
  export default {
    data() {
      return {
        user: {
          name: '叶泽坤',
          description: '我是一个大学霸',
          avatar: require('../../assets/logo.png')
        }
      }
    }
  }
</script>

<style>
  #user-setting {
    background-color: grey;
  }
</style>