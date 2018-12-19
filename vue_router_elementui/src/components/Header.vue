<template>
    <el-row>
      <el-col :span="24">
        <div class="header-wrap">{{title}}</div>
      </el-col>
    </el-row>
</template>

<script>
export default {
  name: 'Header',
  props: ['title']
}
</script>

<style scoped>
.header-wrap{

}
</style>
