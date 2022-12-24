<template>
  <div id="app">
      <sidebar-menu/>
      <Home/>
      <About/>
      <Directions/>
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
    import Directions from "@/components/Directions";

export default {
  name: 'App',
  components: {
      Directions,
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
h2{
    text-transform: uppercase;
    text-shadow: 1px 1px 1px #001056;
    color: #77AEDB;
    font-size: 2.5rem !important;
}
h3{
    text-shadow: .5px .5px .8px #000;
    color: #77AEDB;
}
b, u, p, li, .text{
    font-size: 1.2rem;
    line-height: 1.8rem;
}
b, u, p, li, .text, button{
    font-family: Verdana,Geneva,sans-serif,"websafe";
}
button{
    font-size: 1.5rem;
    border-radius: 30px;
    background: linear-gradient(to left, #b7dfe9,#adc7e2, #a0a6d8);
    a{
        color:white;
        text-decoration: none;
    }
}
#Home, #About, #Directions, #Advantages, #Employees, #Services, #Contacts{
    padding: 2% 3% 2% 5%;
}
#Home{
    h1{
        margin-top: 4%;
        font-size: 3.5rem;
        line-height: 4rem;
        width: 110%;
        font-weight: 600;
    }
    p{
        margin: 4% 0;
        font-size: 1.35rem;
        line-height: 2.25rem;
    }
    button{
        width: 48%;
        margin: 3% 1.5%;
        padding: 2%;
        font-size: 1.5rem;
        border-radius: 30px;
        border: none;
        &:last-child{
            margin-top: 2%;
        }
    }
    svg{
        margin-top: 2%;
        width: 100%;
    }
}
#Directions{
        .wrapper {
            display: flex;
            flex-wrap: wrap;
            div{
                width: 100%;
                margin: 0 auto 1%;
            }
        }
        ul {
            margin-bottom: 0 !important;
            list-style: none !important;
        }
        li:before {
            padding-right:10px;
            margin-left: -3%;
            font-size: 2rem;
            color: #77AEDB;
            content: "\2727";
        }
        li:hover:before {
            color: #337AB7;
            content: "\2726";
        }
    }
</style>
