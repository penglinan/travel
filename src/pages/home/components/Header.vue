<template>
  <div class="header">
    <div class="header-left"><span class="iconfont">&#xe605;</span></div>
    <div class="header-input"><span class="iconfont">&#xe6e4;</span>请输入城市/景点/游玩主题</div>
    <div class="header-right">城市<span class="iconfont">&#xe68f;</span></div>
  </div>
</template>
<script>
export default {
  name: 'Header'
}
</script>
<style lang="stylus" scoped>
.header
  display:flex
  height:0.86rem
  background:#00bcd4
  color:#fff
  line-height:.86rem
  .header-left
    width:0.64rem
    float:left
  .header-input
    flex:1
    background:#fff
    height:0.64rem
    line-height:.64rem
    margin:0.12rem 0 0 0.2rem
    border-radius:.1rem
    color:#ccc
  .header-right
    width:1.24rem
    flaot:right
    text-align:center

</style>
