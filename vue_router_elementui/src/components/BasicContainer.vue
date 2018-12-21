<template>
  <div>
    <slot>我是插槽，父组件不传值就显示我，传值就显示父组件的传值</slot>
  </div>
</template>

<script>
export default {
  name: 'BasicContainer'
}
</script>

<style scoped>

</style>
