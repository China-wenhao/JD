<template>
  <div class="wrapper">
    <div class="position">
      <span class="iconfont position__icon">&#xe608;</span>
      北京理工大学国防科技园2号楼10层
      <span class="iconfont position_notice">&#xe64e;</span>
    </div>
    <div class="search">
      <span class="iconfont">&#xe67d;</span>
      <span class="search__text">山姆会员商店优惠商品</span>
    </div>
    <div class="banner">
      <img
        class="banner__img"
        src="http://www.dell-lee.com/imgs/vue3/banner.jpg"
      />
    </div>
    <div class="icons">
      <div class="icons__item" v-for="item in iconsList" :key="item.desc">
        <img
          class="icons__item__img"
          :src="`http://www.dell-lee.com/imgs/vue3/${item.imgName}.png`"
        />
        <p class="icons__item__desc">{{ item.desc }}</p>
      </div>
    </div>
    <div class="gap"></div>
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

<script>
  export default{
    name:"StaticPart",
    data(){
      return{
        iconsList : [
      { imgName: "超市", desc: "超市便利"},
      { imgName: "菜市场", desc: "菜市场"},
      { imgName: "水果店", desc: "水果店"},
      { imgName: "鲜花", desc: "鲜花绿植"},
      { imgName: "医药健康", desc: "医药健康"},
      { imgName: "家居", desc: "家居时尚"},
      { imgName: "蛋糕", desc: "烘培蛋糕"},
      { imgName: "签到", desc: "签到"},
      { imgName: "大牌免运", desc: "大牌免运"},
      { imgName: "红包", desc: "红包套餐"},
    ]
      }
    }
  }
</script>

<style lang="scss">
@import "./style/viriables.scss";
@import "./style/mixins.scss";
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
  padding: 0.16rem 0.24rem 0.16rem 0;
  line-height: 0.22rem;
  font-size: 0.16rem;
  @include ellipse;
  .position__icon {
    position: relative;
    top: 0.01rem;
    font-size: 0.2rem;
  }
  .position_notice {
    position: absolute;
    right: 0;
    top: 0.17rem;
    font-size: 0.2rem;
  }
  color: $content-fontcolor;
}
.search {
  margin-bottom: 0.12rem;
  line-height: 0.32rem;
  background: #ddd;
  color: #434;
  border-radius: 0.16rem;
  .iconfont {
    display: inline-block;
    padding: 0 0.08rem 0 0.16rem;
    font-size: 0.16rem;
  }
  &__text {
    display: inline-block;
    font-size: 0.14rem;
  }
}
.banner {
  height: 0;
  overflow: hidden;
  padding-bottom: 25.4%;
  &__img {
    width: 100%;
  }
}
.icons {
  display: flex;
  flex-wrap: wrap;
  margin-top: 0.16rem;
  &__item {
    width: 20%;
    &__img {
      display: block;
      width: 0.4rem;
      height: 0.4rem;
      margin: 0 auto;
    }
    &__desc {
      margin: 0.06rem 0 0.16rem 0;
      text-align: center;
      color: $content-fontcolor;
    }
  }
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
  color: $content-fontcolor;
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
.gap {
  margin: 0 -0.18rem;
  height: 0.1rem;
  background: $content-bgColor;
}
</style>
