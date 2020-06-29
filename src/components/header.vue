<template>
  <header class="am-topbar am-topbar-inverse admin-header">
    <div class="am-topbar-brand">
      <router-link to="/"><strong>深海如梦</strong></router-link>
    </div>

    <div class="am-collapse am-topbar-collapse" id="topbar-collapse">
      <ul class="am-nav am-nav-pills am-topbar-nav am-topbar-right admin-header-list">
        <li>
          <a href="/">
            <span class="am-icon-home"></span> 首页
          </a>
        </li>
      </ul>
    </div>
  </header>
</template>
<script>
export default {
  name: "Header"
};
</script>