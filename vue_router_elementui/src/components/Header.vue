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
  // props 传递不带验证
  // props: ['title']
  // props 传值附带验证，此处验证传过来的值必须为Number，否则会在console 中报错
  props: {
    title: {
      type: Number,
      request: true
    }
  }
}
</script>

<style scoped>
.header-wrap{

}
</style>
