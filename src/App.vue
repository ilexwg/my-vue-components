<template>
  <div id="app">
    <wg-button @click="onClick">Hello button</wg-button>
    <wg-button @click="onClick" type="">Hello button</wg-button>
    <wg-button @click="onClick" type="">Hello button</wg-button>
  </div>
</template>

<script>
import WgButton from './components/WgButton/WgButton';

export default {
  name: 'app',
  components: {
    WgButton
  },
  methods: {
    onClick() {
      console.log('click');
    }
  }
}
</script>

<style lang="less">
</style>
