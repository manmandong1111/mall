<template>
  <tab-bar>
    <tab-item link='/home'>
      <img src="~assets/img/tabbar/home.svg" slot="item-icon">
      <img src="~assets/img/tabbar/home_active.svg" slot="item-active-icon">
      <div slot="item-text">首页</div>
    </tab-item>
    <tab-item link='/category'> 
      <img src="~assets/img/tabbar/category.svg" slot="item-icon">
      <img src="~assets/img/tabbar/category_active.svg" slot="item-active-icon">
      <div slot="item-text">分类</div>
    </tab-item>
    <tab-item link='/cart'> 
      <img src="~assets/img/tabbar/shopcart.svg" slot="item-icon">
      <img src="~assets/img/tabbar/shopcart_active.svg" slot="item-active-icon">
      <div slot="item-text">购物车</div>
    </tab-item>
    <tab-item link='/profile'> 
      <img src="~assets/img/tabbar/profile.svg" slot="item-icon">
      <img src="~assets/img/tabbar/profile_active.svg" slot="item-active-icon">
      <div slot="item-text">我的</div>
    </tab-item>
  </tab-bar>
</template>

<script>
import TabBar from 'components/common/tabBar/TabBar'
import TabItem from 'components/common/tabBar/TabItem'

export default {
  name: 'MainTabBar',
  components: {
    TabBar,
    TabItem
  }
}
</script>

<style>

</style>