<template>
  <div>
    <div class="title">热门推荐</div>
    <ul class="menu">
      <li @click="menu1">笔记本电脑</li>
      <li @click="menu2">手机0</li>
      <li @click="menu3">手机1</li>
      <li>手机2</li>
      <li>手机3</li>
      <li>手机4</li>
      <li>手机5</li>
      <li>手机6</li>
      <li>手机7</li>
      <li>手机8</li>
      <li>手机9</li>
      <li>手机10</li>
    </ul>
  </div>
</template>
<style>
  .title{
    color: red;
    width: 100px;
    font-size: 20px;
  }
  .menu li{
    list-style: none;
    height:50px;
    margin-bottom: 2px;
    background-color: white;
    line-height: 50px;
    cursor: pointer;
  }
</style>
<script>
import Msg from './Msg.js'
export default {
  methods: {
    menu1: function () {
      Msg.$emit('val', 1)
    },
    menu2: function () {
      Msg.$emit('val', 2)
    },
    menu3: function () {
      Msg.$emit('val', 3)
    }
  }
}
</script>
