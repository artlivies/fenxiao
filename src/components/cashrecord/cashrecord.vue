<template>
  <transition name="slide">
    <div class="cashrecord">
      <div class="top">
        <div class="back" @click="back"><span class="iconfont icon-jiantouarrowhead7"></span></div>
        <div class="box acea-row row-between-wrapper">
          <div class="fl">
            <div class="name">提现记录</div>
            <div class="num">￥<span>0</span></div>
          </div>
          <div class="fr">
            <span class="iconfont icon-jiludanzilishijilu"></span>
          </div>
        </div>
      </div>
      <div class="list">
        <van-row type="flex" justify="center" class="list_nav">
          <van-col span="8">提现时间</van-col>
          <van-col span="8">提现金额(元)</van-col>
          <van-col span="8">状态</van-col>
        </van-row>
        <van-row type="flex" justify="center" class="list_item">
          <van-col span="8">2020-02-21</van-col>
          <van-col span="8">99.8</van-col>
          <van-col span="8">进行中</van-col>
        </van-row>
        <van-row type="flex" justify="center" class="list_item">
          <van-col span="8">2020-02-23</van-col>
          <van-col span="8">11.3</van-col>
          <van-col span="8">成功</van-col>
        </van-row>
      </div>
    </div>
  </transition>
</template>

<script type="text/ecmascript-6">
export default {
  data () {
    return {
    }
  },
  methods: {
    back () {
      this.$router.back()
    }
  }
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  @import "~common/stylus/variable"
  .cashrecord
    position fixed
    top 0
    bottom 0
    z-index 100
    width 100%
    background #f5f5f5
    &.slide-enter-active, &.slide-leave-active
      transition: all .3s
    &.slide-enter, &.slide-leave-to
      transform: translate3d(100%, 0, 0)
    .top
      background linear-gradient(to right, #fd972b , #fc6416)
      height 2.2rem
      width 100%
      position relative
      color #fff
      .back
        position absolute
        left 0
        top 0
        width 1rem
        line-height 1rem
        text-align center
        .iconfont
          font-size .4rem
      .box
        padding 0 1rem
        width 100%
        height 100%
        box-sizing border-box
        .fl
          font-size .28rem
          .num
            margin-top .1rem
            span
              font-size .5rem
        .fr
          .iconfont
            font-size 1rem
      .item
        float left
        width 50%
        position relative
        &.active
          color #fc8535
          &:after
            content ''
            position absolute
            width .5rem
            height 2px
            background #fc8535
            bottom 0
            left 50%
            margin-left -.25rem
    .list
      font-size .28rem
      .list_nav
        background #fff
        border-top 1px solid #eee
        border-bottom 1px solid #eee
        height 0.86rem
        line-height 0.86rem
        text-align center
      .list_item
        background #fff
        border-bottom 1px solid #eee
        height 0.86rem
        line-height 0.86rem
        text-align center
</style>
