<template>
  <footer>
    <p>{{ footerText }}</p>
  </footer>
</template>

<script>
export default {
data() {
    return {
        footerText: 'This is The Footer'
    }
}
}
</script>

<style>
footer {
 
max-height: 100px;
height: 100%;
flex-direction: column;
text-align: center;
box-shadow: 0px 6px 9px rgba(0, 0, 0, 0.25); 
  display: flex;
  flex-direction:column;
  transition: 0.3s ease ;
  background: #e6fa30;
  font-family: 'Quicksand', sans-serif;
  position: fixed;
  z-index: 1;
  bottom: 0;
  padding: 0.5em;
  width: 100%;
  font-family: 'Quicksand', sans-serif;
  font-weight: 500;
  font-size: larger;
  margin-left: -10px;
  
}

</style>