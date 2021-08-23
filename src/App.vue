<template>
  <img alt="Vue logo" :src="hehe" />
  <HelloWorld msg="Hello Vue 3 + Vite" />
  <div class="test">
    <span class="test__one">awdasfewd</span>
    <span class="test__two">{{test}}44</span>
  </div>
  
  
  <!-- {{hehe}} -->
  <!-- {{import.meta.env.MODE}} -->
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import imgUrl from '../public/favicon.ico';


export default {
  components: {HelloWorld},
  data() {
    return {
      test: 1,
      hehe: imgUrl
    }
  },
  created() {
    // env meta tag 접근
    console.log(import.meta.env)
    // this.hehe = import.meta.env.MODE;
  }
}


// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/master/active-rfcs/0040-script-setup.md
</script>

<style lang="scss" scoped>
/* scss - yarn add -D sass 만 하고 lang 추가만하면됨 node-sass 설치할 필요없음 */
.test {
  display: flex;
  justify-content: center;
  &__one {
    color: red;
  }
  &__two {
    color: blue;
  }
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
