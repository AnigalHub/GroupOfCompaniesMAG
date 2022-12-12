<template>
  <div id="app">
      <sidebar-menu/>
      <Home/>
      <About/>
      <Advantages/>
      <Employees/>
      <Services/>
      <Contacts/>
  </div>
</template>

<script>
    import SidebarMenu from "@/components/SidebarMenu.vue"
    import Home from './components/Home.vue'
    import About from "@/components/About";
    import Advantages from "@/components/Advantages";
    import Employees from "@/components/Employees";
    import Services from "@/components/Services";
    import Contacts from "@/components/Contacts";

export default {
  name: 'App',
  components: {
      Contacts,
      Services,
      Employees,
      Advantages,
      About,
      Home,
      SidebarMenu,
  }
}
</script>

<style lang="scss">
    @import url('https://unpkg.com/boxicons@2.0.7/css/boxicons.min.css');
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
h3{
    text-shadow: .5px .5px .8px #000;
    color: #77AEDB;
}
b,u, p,li,.text{
    font-size: 1.2rem;
    line-height: 1.8rem;
    font-family: Verdana,Geneva,sans-serif,"websafe";
}
button{
    font-family: Verdana,Geneva,sans-serif,"websafe";
}
</style>
