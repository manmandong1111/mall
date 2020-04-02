<template>
  <div class="tab-bar">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'TabBar'
}
</script>

<style scoped>
  .tab-bar {
    height: 49px;
    background-color: #f6f6f6;
    border-top: 1px solid #eee;
    box-shadow: 0px -1px 1px rgba(150,150,150,.08);

    position: fixed;
    bottom:0;
    left: 0;
    right: 0;

    display: flex;
    text-align: center;
  }
</style>