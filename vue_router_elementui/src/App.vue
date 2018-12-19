<template>
  <div id="app">

    <el-container>
      <el-header>
        <mheader class="header" :title="titleText"></mheader>
      </el-header>
      <el-container>
        <el-aside width="200px">
          <navmenu></navmenu>
        </el-aside>
        <el-main><router-view></router-view></el-main>
      </el-container>
    </el-container>

  </div>
</template>

<script>
import NavMenu from '@/components/NavMenu'
import Header from '@/components/Header'
export default {
  name: 'App',
  data  () {
    return {
      titleText: 0
    }
  },
  components: {
    'navmenu': NavMenu,
    'mheader': Header
  }
}
</script>

<style>
.header {
  background-color: #409EFF;
  color: #fff;
  line-height: 60px;
}
</style>
