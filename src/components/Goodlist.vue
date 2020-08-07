<template>
  <div name="show">
    <ul class="goodlist">
      <li v-for="goods in list" :key="goods">
        <img v-bind:src="goods.img">
        <p>{{goods.name}}</p>
      </li>
    </ul>
  </div>
</template>
<style>
  .goodlist li{
    width: 200px;
    height: 200px;
    list-style: none;
    float: left;
    font-size: 9px;
    color: red;
    margin-bottom: 30px;
  }
  .goodlist img{
    width: 180px;
    height: 180px;
  }
</style>
<script>
export default {
  name: 'show',
  data () {
    var _this = this
    var url = ''
    if (_this.goodId === 1) {
      url = 'json/bjb.json'
    } else if (_this.goodId === 2) {
      url = 'json/shouji.json'
    }
    this.$http.get(url).then(function (res) {
      _this.list = res.data
    })
    return {
      list: []
    }
  },
  props: {
    goodId: Number
  },
  watch: {
    goodId () {
      var _this = this
      var url = ''
      if (_this.goodId === 1) {
        url = 'json/bjb.json'
      } else if (_this.goodId === 2) {
        url = 'json/shouji.json'
      }
      this.$http.get(url).then(function (res) {
        _this.list = res.data
      })
      return {
        list: []
      }
    }
  }
}
</script>
