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
h1{
    margin-top: 4% !important;
    font-size: 3.5rem !important;
    line-height: 4rem !important;
    width: 110%;
    font-weight: 600 !important;
}
h2{
    text-transform: uppercase;
    text-shadow: 1px 1px 1px #001056;
    color: #77AEDB;
    font-size: 2.5rem !important;
    margin-bottom: 2% !important;
}
h3{
    text-shadow: .5px .5px .8px #000;
    color: #77AEDB;
}
a{
    text-decoration: none;
}
b, u, p, li, .text{
    font-size: 1.18rem;
    line-height: 1.8rem;
}
b, u, p, li, .text, button{
    font-family: Verdana,Geneva,sans-serif,"websafe";
}
ul{
    list-style: none !important;
    margin-bottom: 1.5% !important;
}
li{
    margin-bottom: 2.25%;
}
li:before {
    font-weight: bold;
    padding-right:10px;
    margin-left: -3%;
    font-size: 2rem;
    color: #77AEDB;
    transition-duration: 0.5s;
}
li:hover:before {
    color: #337AB7;
}
button{
    font-size: 1.5rem !important;
    border-radius: 30px !important;
    border: none !important;
    text-shadow: 1px 1px 0.2px rgb(0 0 0 / 43%) !important;
    background: linear-gradient(to left, #b7dfe9,#adc7e2, #a0a6d8);
    a{
        color:white;
        text-decoration: none;
    }
}
#Home, #About{
    svg{
        width: 100%;
    }
}
#Advantages, #Employees, #Services{
    svg{
        width: 90%;
    }
}
#About, #Services{
    li:before {
        content: "\25cb";
    }
    li:hover:before {
        content: "\25cf";
    }
}
#Advantages, #Services{
    button{
        width: 60%;
        margin: 1% 1.5%;
        padding: 1.5%;
    }
}
#Home, #About, #Directions, #Advantages,
#Employees, #Services, #Contacts{
    padding: 2% 3% 2% 5%;
}
#Home{
    p{
        margin: 4% 0;
        font-size: 1.35rem;
        line-height: 2.25rem;
    }
    button{
        width: 48%;
        margin: 3% 1.5%;
        padding: 2%;
        border: none;
        &:last-child{
            margin-top: 2%;
        }
    }
    svg{
        margin-top: 2%;
    }
}
#About{
    h2{
        margin-top: 5%;
    }
    li{
        margin-bottom: 0;
    }
}
#Directions{
    .col{
        padding: 0 !important;
    }
    .col-3 {
        width: 21% !important;
    }
    .wrapper {
        display: flex;
        flex-wrap: wrap;
        div{
            width: 100%;
            margin: 0 auto 1%;
        }
    }
    li:before {
        content: "\2727";
    }
    li:hover:before {
        content: "\2726";
    }
}
#Advantages{
    ul li:before {
        content: "\1F5F8";
    }
    ul li:hover:before {
        content: "\2713";
    }
    .col-1 svg{
        width: 2.8rem;
        margin-top: 45%;
        margin-right: 15%;
    }
    svg{
        margin-top: -5%;
    }
}
#Employees{
    svg{
        margin-top: -3%;
    }
    ul li:before {
        content: "\2606";
    }
    ul li:hover:before {
        content: "\2605";
    }
    h2 span{
        text-shadow: none;
        text-transform: lowercase;
    }
}
#Services{
    svg{
        margin-top: -5%;
    }
}
#Contacts{
    .contacts{
        padding-left: 2%;
    }
    span{
        font-weight: 600;
        text-decoration: underline;
    }
    a{
        margin-top: 5%;
    }
    .nameContact{
        padding: 1.5%;
        svg{
            width: 2.5rem;
            margin-top: 40%;
        }
    }
    svg{
        width: 95%;
        margin-top: -2%;
    }
}
</style>
