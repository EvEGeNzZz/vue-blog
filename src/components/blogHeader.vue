<template>
  <div class="header">
    <ul class="menu">
      <li class="menu-item" style="margin-left: 0;">
        <a href="/" class="menu-link menu-logo">
          <img src="/static/images/logo.png" alt="" class="menu-img"><span class="hide-on-mobile">Вастрик</span>
        </a>
      </li>
      <li class="menu-item menu-item_active_yes"><a href="/blog/" class="menu-link">Блог</a></li>
      <li class="menu-item "><a href="/world/" class="menu-link">Мир</a></li>
      <li class="menu-item "><a href="/donate/" class="menu-link">Донат</a></li>
      <li class="menu-item menu-item__login"><a href="/club/" class="menu-link">Клуб</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'blogHeader'
}
</script>

<style>
.header {
  position: relative;
  z-index: 9999;
  width: 100%;
  min-width: 320px;
  font-size: 17px;
  height: 50px;
  margin: 0 auto;
  background: rgba(0, 0, 0, 0.7);
}
.menu {
  position: relative;
  display: block;
  width: 100%;
  min-width: 320px;
  height: 50px;
  margin: 0 auto;
  padding-left: 10px;
  box-sizing: border-box;
  overflow: hidden;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  z-index: 1002;
}
.menu-item {
  margin: 0;
  position: relative;
  list-style-type: none;
  height: 50px;
  margin-left: 2%;
  line-height: 43px;
  vertical-align: top;
  display: inline-block;
  font-weight: normal;
  font-style: normal;
}
.menu-link:hover, .menu-item_active_yes {
  opacity: 0.5;
  -webkit-transition: opacity 0.2s ease-in;
  -moz-transition: opacity 0.2s ease-in;
  -o-transition: opacity 0.2s ease-in;
  -ms-transition: opacity 0.2s ease-in;
  transition: opacity 0.2s ease-in;
}
.menu-item__login {
  float: right;
  background-color: #000;
  max-width: 300px;
  min-width: 50px;
  text-align: center;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.menu-link {
  cursor: pointer;
  display: inline-block;
  vertical-align: middle;
  color: #FFF;
  text-decoration: none;
  padding: 0 10px;
  outline-offset: -0.22222em;
  -webkit-tap-highlight-color: transparent;
  -webkit-transition: opacity .2s cubic-bezier(0.645,0.045,0.355,1);
  -moz-transition: opacity .2s cubic-bezier(0.645,0.045,0.355,1);
  transition: opacity .2s cubic-bezier(0.645,0.045,0.355,1);
}
</style>