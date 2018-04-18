<template>
  <div class="header">
    <div class="header-left"><span class="iconfont back-icon">&#xe605;</span></div>
    <div class="header-input"><span class="iconfont">&#xe6e4;</span>请输入城市/景点/游玩主题</div>
    <div class="header-right">城市<span class="iconfont arrow-icon">&#xe68f;</span></div>
  </div>
</template>
<script>
export default {
  name: 'Header'
}
</script>
<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
.header
  display:flex
  height:0.86rem
  background:$bgColor
  color:#fff
  line-height:.86rem
  .header-left
    width:0.64rem
    float:left
    .back-icon
      text-align:center
      font-size: .4rem
      display:block
  .header-input
    flex:1
    background:#fff
    height:0.64rem
    line-height:.64rem
    margin:0.12rem 0 0 0.2rem
    border-radius:.1rem
    color:#ccc
    padding-left: .2rem
  .header-right
    width:1.24rem
    flaot:right
    text-align:center
    .arrow-icon
      font-size: .1rem
      margin-left: .1rem

</style>
