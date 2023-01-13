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
    margin-top: 9% !important;
    font-size: 4rem !important;
    color: #5d86b4;
    font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
    font-weight: 700 !important;
    line-height: 4.7rem !important;
    padding-bottom: 2% !important;
    width: 110%;
}
h2{
    color: #5d86b4;
    font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
    font-weight: 700 !important;
    font-size: 2.8rem !important;
    margin-bottom: 2% !important;
}
h3{
    text-shadow: .5px .5px .8px #000;
    color: #77AEDB;
}
a{
    text-decoration: none;
}
.sidebar li {
    font-size: 1.2rem;
}
b, u, p, li, .text, a{
    font-size: 1.24rem;
    line-height: 1.8rem;
}
a, b, u, p, li, .text, button, .sidebar li{
    font-weight: 400;
    font-family: Circular,-apple-system,BlinkMacSystemFont,Roboto,Helvetica Neue,sans-serif !important;
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
    padding-right: 10px;
    margin-left: -3%;
    font-size: 2rem;
    color: #77AEDB;
    transition-duration: 0.5s;
}
li:hover:before {
    color: #337AB7;
}
button{

    border-radius: 30px !important;
    border: none !important;
    background: linear-gradient(to left, #a9d3dd, #9ba0cb);
    a{
        color:white;
        font-size: 1.3rem !important;
        font-weight: 500;
        text-decoration: none;
    }
}
#Home, #About{
    svg{
        width: 100%;
    }
}
#Advantages, #Services{
    svg{
        width: 95%;
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
    padding: 2% 3% 2% 6%;
}
#Home{
    p{
        margin: 4% 0;
        font-size: 1.35rem;
        line-height: 2.25rem;
    }
    button{
        width: 60%;
        margin: 3% 1.5%;
        padding: 2.7% 2.5%;
        border: none;
        &:last-child{
            margin-top: 2.5%;
        }
    }
    svg{
        margin-top: 2%;
        width: 105%;
        margin-left: -5%;
    }
}
#About{
    h2{
        margin-top: 5%;
    }
    li{
        margin-bottom: 0;
    }
    svg{
        margin-top: 5%;
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
        margin-left: -8%;
        width: 108%;
    }
    ul li:before {
        content: "\2606";
    }
    ul li:hover:before {
        content: "\2605";
    }
    h2 span{
        text-shadow: none;
        font-weight: 400;
        text-transform: lowercase;
        text-decoration: none;
    }
    span{
        font-weight: 600;
    }
}
#Services{
    svg{
        margin-top: -5%;
    }
}
#Contacts{
    padding-bottom: 3%;
    .contacts{
        margin-left: - 2%;
    }
    span{
        font-weight: 600;
        text-decoration: underline;
    }
    a{
        margin-top: 5%;
    }
    svg{
        margin-top: 5%;
        margin-left: -8%;
        width: 112%;
    }
    .nameContact{
        padding: 1%;
        svg{
            width: 2.5rem;
            margin-top: 15%;
        }
    }
}
@media screen and (min-width: 768px) and (max-width: 992px){

}
</style>
