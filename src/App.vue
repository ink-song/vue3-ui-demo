<template>
  <DefaultLayouts :menus="menus" />
</template>

<script>
import DefaultLayouts from '@/layouts/default/index.vue'
const menus = [
  {
    title: '首页',
    name: '1111',
  },
  {
    title: '个人中心',
    name: '121312',
  },
]
export default {
  name: 'app',
  components: {
    DefaultLayouts,
  },
  setup() {
    return {
      menus,
      // menus: ref<string[{}]>(["2"])
    }
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
