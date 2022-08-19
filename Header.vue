<template>
  <header>
      <h1>
       {{ title }}
      </h1>
      <div class="login">  
        <router-link v-bind:to="{ name: 'login' }">Login</router-link>
      </div>
    </header>
    
</template>

<script>
export default {
data() {
    return {
        title: 'Hello Welcome to the Header!'
    }
}
}
</script>

<style>
/* styling for header */
header {
max-height: 100px;
height: 100%;
flex-direction: column;
text-align: center;
box-shadow: 0px 6px 9px rgba(0, 0, 0, 0.25); 
  display: flex;
  flex-direction:column;
  transition: 0.3s ease ;
  background: #ab4ec7;
  font-family: 'Quicksand', sans-serif;
  float: top;
  position: fixed;
  z-index: 1;
  top: 0;
  bottom: 0;
  padding: 0.5em;
  width: 100%;
  justify-content: flex-start;
}

h1 {
  font-family: 'Holtwood One SC', serif;
}  
.login {
  display: flex;
  flex-direction: row;
  margin-left: 1700px;
  margin-top: -90px;
  border-radius: 10px;
  font-size: 200%;
  
 

}
</style>