<template>
  <el-menu class="navbar" mode="horizontal">
    <hamburger 
      class="hamburger-container"
      :toggleClick="toggleSideBar"
      :isActive="!sidebar.opened">
    </hamburger>
    <div class="right-menu">
      <screenfull class="screenfull"></screenfull>
      <div class="lang">
        <el-dropdown>
          <i class="iconfont icon-language4"></i>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item @click.native="toggleLang('zh')" :disabled="$i18n.locale == 'zh'">中文</el-dropdown-item>
            <el-dropdown-item @click.native="toggleLang('en')" :disabled="$i18n.locale == 'en'">English</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </div>
      <theme-picker></theme-picker>
    </div>
  </el-menu>
</template>