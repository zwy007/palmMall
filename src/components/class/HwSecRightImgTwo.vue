<template>
  <li>
    <img :src="produce" alt="">
  </li>
</template>

<script>
    export default {
        name: "HwSecRightImgTwo",
      props:["produce"]
    }
</script>

<style scoped>
  .tjclass li{
    width:30%;
    margin-right: .06rem;
    flex-shrink: 0;
    flex-wrap: nowrap;
  }
  .tjclass li img{
    border-radius:4px;
    height:.38rem;
    width:100%;
  }
</style>
