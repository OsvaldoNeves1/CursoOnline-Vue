<template>
  <div id="app">
    <TheHeader/>
    <main id="main">
      <router-view class="container"></router-view>
    </main>
    <TheFooter/>
  </div>
</template>

<script>
import TheHeader from "@/components/TheHeader.vue";
import TheFooter from "@/components/TheFooter.vue";



export default {
  components: {
    TheHeader,
    TheFooter
  }
  
}
</script>

<style>

body {
  margin: 0px;
  font-family: 'Raleway', sans-serif;
  color: #234;
  background: url("./assets/pattern.svg");
}
ul {
  list-style: none;
  padding: 0px;
  margin: 0px;
  
}

a {
  font-weight: bold;
  text-decoration: none;
  color: #234;
}

a.router-link-exact-active {
  color: #4b8;
}

.container {
  max-width: 950px;
  margin: 0 auto;
  padding: 20px;
}

.v-enter {
  opacity: 0;
  transform: translate3d(-20px, 0, 0);
}

.v-enter-active{
  transition: all .3s;
}

.conteudo {
  display: grid;
  grid-template-columns: 1fr minmax(200px, 400px);
  grid-gap: 30px;
}

#app {
  display: flex;
  min-height: 100vh;
  flex-direction: column;
}
#main {
  flex: 1;
}

@media screen and (max-width: 500px) {
  .conteudo {
    display: block;
  }
  .conteudo img {
    display: none;
  }
}

</style>
