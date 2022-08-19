<template>
  <div>
    <app-header />
    <app-side-bar />
    <app-right-panel />
    <app-footer />
    <main class="main">
      <div id="text-container">
        <h3>Insert Your Palindrome</h3>
        <input id="input" v-model="userInput" type="text">
        <button v-on:click="checkPalindrome" type="submit">Check!</button>
        <br>
        <label for="input" 
        v-if="isTrue === true"> Thats a Palindrome!</label>
        <label for="input"
        v-if="isTrue === false">Sorry that isn't a Palindrome...</label>
        
      </div>
    </main>    
  </div>
  
</template>
<script>
import Header from '@/views/Header.vue'
import Footer from '@/views/Footer.vue'
import SideBar from '@/views/SideBar.vue'
import RightPanel from '@/views/RightPanel.vue'
export default {
  components: {
   'app-header':Header,
    'app-side-bar':SideBar,
    'app-right-panel':RightPanel,
    'app-footer':Footer, 
    
  }, 
    data () {
      return {
        isTrue: null,
        userInput: ""

      }
    },
    methods: {
      checkPalindrome(stringy) {
        let drome = /[\W_]/g;
        stringy = this.userInput.toLowercase().replace(drome, '');
        let lengthy = stringy.lengthy;
        for (let i = 0; i < lengthy/2; i++){
          if(stringy[i] !== stringy[lengthy -1 - i]){
            return false;
          }
        } 
        return true;
    }
    }
  
}
</script>
<style>
/* importation of all fonts */
@import url('https://fonts.googleapis.com/css2?family=Hind:wght@300;400&family=Holtwood+One+SC&family=Quicksand:wght@300;400;500&display=swap');

#main {
    width: 800px;
    height: 1000px;
    
}
</style>
