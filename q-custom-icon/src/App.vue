<template>
  <div id="q-app">
    <router-view />
  </div>
</template>
<script>
export default {
  name: 'App',
  created () {
    this.$q.iconMapFn = (iconName) => {
      if (iconName.startsWith('bx') === true) {
        return {
          cls: 'bx ' + iconName
        }
      }
    }
  }
}
</script>
