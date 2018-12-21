<template>
    <el-row>
      <el-col :span="24">
        <span :value="dataFromOther" @click="handleClick">{{dataFromOther}}</span>
      </el-col>
    </el-row>
</template>

<script>
export default {
  name: 'Header',
  // props 传递不带验证
  // props: ['title']
  // props 传值附带验证，此处验证传过来的值必须为Number，否则会在console 中报错
  // props: {
  //   title: {
  //     type: Number,
  //     request: true
  //   }
  // }
  // 自定义v-model
  // v-model的语法糖包装：
  // <input v-model="something">
  // <input
  // :value="something"
  // @:input="something = $event.target.value">
  // 所以带有v-model的组件的核心用法为：
  // 带有v-model的父组件通过绑定的value值（即v-model的绑定值）传给子组件，子组件通过 prop接收一个 value;
  // 子组件利用 $emit 触发 input 事件，并传入新值value给父组件；
  data () {
    return {
      mcount: 0,
      dataFromOther: this.fromOther
    }
  },
  model: {
    prop: 'fromOther',
    event: 'change'
  },
  props: {
    // 接收父组件传递过来的值（v-model=“被传递的值”）
    fromOther: {
      type: String
    }
  },
  methods: {
    handleClick () {
      this.mcount += 1
      this.dataFromOther = '我是新值' + (this.mcount)
      // 触发事件，并传入新值
      this.$emit('handleClick')
    }
  }
}
</script>

<style scoped>
.header-wrap{
 padding:0;
  margin:0;
}
</style>
