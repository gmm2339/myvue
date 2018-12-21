<template>
  <div id="app">

    <el-container>
      <el-header>
        <!-- 自定义v-model="titleText"应用 此处将titleText 传递给子组件中的props -->
        <mheader class="header"   v-model="titleText"></mheader>
      </el-header>
      <el-container>
        <el-aside width="200px">
          <navmenu></navmenu>
        </el-aside>
        <el-main><router-view>我给卡槽提供数据</router-view></el-main>
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
      titleText: '我来测试自定义v-model'
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
