<template>
  <div>
    <mbp-header />
    <router-view />
  </div>
</template>

<script>
import MbpHeader from "./components/MbpHeader";
export default {
  components: {
    MbpHeader,
  }
}
</script>

<style lang="less">
html {
  font-size: 16px;
}

body {
  background: #5b5c71;
  font: 500 1rem Heebo;
  margin: 1rem; 
}
</style>