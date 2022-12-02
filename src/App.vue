<template>
  <div id="app">
      <sidebar-menu/>
      <Home/>
      <About/>
      <Advantages/>
      <Employees/>
  </div>
</template>

<script>
    import SidebarMenu from "@/components/SidebarMenu.vue"
    import Home from './components/Home.vue'
    import About from "@/components/About";
    import Advantages from "@/components/Advantages";
    import Employees from "@/components/Employees";

export default {
  name: 'App',
  components: {
      Employees,
      Advantages,
      About,
      Home,
      SidebarMenu,
  }
}
</script>

<style lang="scss">
#app {
    height: 100%;
    margin: 0 !important;
    padding: 0 !important;
    background: #edf8fc;
}
/*контейнер на блоки посередине экрана*/
.container{
    padding-right: 15px !important;
    padding-left: 15px !important;
}
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
button{
    cursor: pointer;
    appearance: none;
    border: none;
    outline: none;
    background: none;
}
h2{
    text-transform: uppercase;
    text-shadow: 1px 1px 2px #000;
    color: #77AEDB;
    font-size: 2.5rem !important;
}
</style>
