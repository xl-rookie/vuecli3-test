<template>
  <div>
    <div v-if="kk==1">
      <Goodlist :goodId="1"></Goodlist>
    </div>
    <div v-if="kk==2">
      <Goodlist :goodId="2"></Goodlist>
    </div>
    <div v-if="kk==3">
      33333
    </div>
  </div>
</template>
<script>
import Msg from './Msg.js'
import Goodlist from './Goodlist.vue'
export default {
  data () {
    return {
      kk: 0
    }
  },
  mounted: function () {
    var _this = this // 添加副本
    Msg.$on('val', function (m) {
      _this.kk = m
    })
  },
  components: {
    Goodlist
  }

}

</script>
