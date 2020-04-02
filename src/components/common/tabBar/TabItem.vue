<template>
  <div class="tab-item" @click="itemClick"> 
    <div class="item-icon" v-if="!isActive"><slot name="item-icon"></slot></div>
    <div class="item-active-icon" v-else><slot name="item-active-icon"></slot></div>
    <div class="item-text" :style='activeStyle'><slot name="item-text"></slot></div>
  </div>
</template>

<script>
export default {
  name: 'TabItem',
  props:{
    link: String
  },
  computed: {
    isActive(){
      return this.$route.path.indexOf(this.link) !== -1
    },
    activeStyle(){
      return this.isActive?{'color':'red'}:{}
    }
  },
  methods:{
    itemClick(){
      this.$router.replace(this.link)
    }
  }
}
</script>

<style scoped>
  .tab-item {
    flex: 1;
  }
  .item-icon img,.item-active-icon img{
    width: 24px;
    height: 24px;
    margin-top: 5px;
    vertical-align: middle;
  }
  .item-text {
    font-size: 12px;
    color: #333;
    margin-top: 3px;
  }
</style>