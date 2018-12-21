<template>
  <div>
    <button @click = 'tabComponent' class = 'btn'>动态组件</button>
    <keep-alive>
      <component v-bind:is="currComponent"></component>
    </keep-alive>
  </div>
</template>
<script>
import DynComponent1 from '../views/DynamicComponent_1'
import DynComponent2 from '../views/DynamicComponent_2'
export default {
  name: 'BasicLayout',
  data () {
    return {
      currComponent: 'DynComponent1',
      arr: ['DynComponent1', 'DynComponent2']
    }
  },
  components: {
    DynComponent1,
    DynComponent2
  },
  methods: {
    tabComponent: function () {
      if (this.currComponent === this.arr[0]) {
        this.currComponent = this.arr[1]
        console.log(this.currComponent)
      } else {
        this.currComponent = this.arr[0]
        console.log(this.currComponent)
      }
    }
  }
}
</script>

<style scoped>
.btn {
  width:100px;
  height: 30px;
}
</style>
