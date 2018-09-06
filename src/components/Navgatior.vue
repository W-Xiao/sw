<template>
  <div class="nav-box">
    <div class="nav-box-out">
      <img src="../img/navImg/logo.jpg" class="logo">
        <div
          v-for="(nav,index) in navs"
          :key="index"
          class="nav-topic"
          :class="{ active:changeColor == index }"
          @click="change(index)">
          {{ nav }}
        </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    msg: String
  },
  data() {
    return {
      navs:["网站首页","产品中心","企业文化","优惠活动","联系我们"],
      changeColor: 0
    }
  },
  methods:{
    change(index){
      this.changeColor = index
      this.$emit("changeIndex", index)
    }
  }
}
</script>

<style scoped>
  @import '../css/Nav.css';
</style>

