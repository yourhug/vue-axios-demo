<template>
  <div>
    <SystemHeader></SystemHeader>
    <div class="am-cf admin-main">
      <router-view></router-view>
    </div>
    <SystemFooter></SystemFooter>
  </div>
</template>

<script>
import SystemHeader from './components/header'
import SystemFooter from './components/footer'
export default{
    name : "App",
    components: {
      SystemHeader,
      SystemFooter,
    }
}
</script>

<style lang="scss">
  @import "./style/style";
  @import "../static/amaze/css/amazeui.css";
  @import "../static/amaze/css/admin.css";
</style>
