<template>
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
.docker {
  box-sizing: border-box;
  display: flex;
  position: absolute;
  left: 0;
  bottom: 0;
  padding: 0 0.12rem;
  width: 100%;
  height: 0.49rem;
  border-top: 1px solid #f1f1f1;
  background-color: #09f;
&__item {
  flex: 1;
  text-align: center;
  .iconfont {
    margin: 0.07rem 0 0.02rem 0;
    font-size: 0.2rem;
  }
  &--active{
    color: #1fa4fc;
  }
}
&__title{
    font-size: .2rem;
    transform: scale(.5,.5);
    transform-origin: center top;
  }
}
</style>
