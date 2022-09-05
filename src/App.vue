<template>
  <div class="wrapper">
    <div class="position">
      <span class="iconfont position__icon">&#xe608;</span>
      北京理工大学国防科技园2号楼10层
      <span class="iconfont position_notice">&#xe64e;</span>
    </div>
  </div>
  <div class="docker">
    <span class="docker__item docker__item--active">
      <div class="iconfont">&#xe600;</div>
      <div class="docker__title">首页</div>
    </span>
    <span class="docker__item">
      <div class="iconfont">&#xe62f;</div>
      <div class="docker__title">购物车</div>
    </span>
    <span class="docker__item">
      <div class="iconfont">&#xe7c5;</div>
      <div class="docker__title">订单</div>
    </span>
    <span class="docker__item">
      <div class="iconfont">&#xe661;</div>
      <div class="docker__title">我的</div>
    </span>
  </div>
</template>

<style lang="scss">
  @import './style/viriables.scss';
  @import './style/mixins.scss';
.wrapper {
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0.5rem;
  right: 0;
  // background: #09f;
  padding: 0 0.18rem;
}
.position {
  position: relative;
  padding: .16rem .24rem .16rem 0;
  line-height: .22rem;
  font-size: .16rem;
  @include ellipse;
  .position__icon {
    position: relative;
    top: .01rem;
    font-size: .2rem;
  }
  .position_notice {
    position: absolute;
    right: 0;
    top: .17rem;
    font-size: .2rem;
  }
  color:$content-font-color;
}
.docker {
  box-sizing: border-box;
  display: flex;
  position: absolute;
  left: 0;
  bottom: 0;
  padding: 0 0.12rem;
  width: 100%;
  height: 0.49rem;
  border-top: 0.01rem solid #f1f1f1;
  // background-color: #09f;
  color:$content-font-color;
  &__item {
    flex: 1;
    text-align: center;
    .iconfont {
      margin: 0.07rem 0 0.02rem 0;
      font-size: 0.2rem;
    }
    &--active {
      color: #1fa4fc;
    }
  }
  &__title {
    font-size: 0.2rem;
    transform: scale(0.5, 0.5);
    transform-origin: center top;
  }
}
</style>
