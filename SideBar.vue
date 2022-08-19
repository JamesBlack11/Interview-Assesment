<template>
  <nav class="left-panel">
<p>{{ sideText }}</p>
    </nav>
</template>

<script>
export default {
data() {
  return {
    sideText: 'Side Bar'
  }
}
}
</script>

<style>
nav {
  display: flex;
  flex-direction:column;
  transition: 0.3s ease ;
  background: #429698;
  float: left;
  position: fixed;
  z-index: 1;
  top: 0;
  bottom: 0;
  left: 0;
  padding: 0.5em;
  max-width: 100px;
  width: 100%;
  text-align: center;
  
}

</style>