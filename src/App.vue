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
    font-weight: 700 !important;
    line-height: 4.9rem !important;
    padding-bottom: 2% !important;
    width: 110%;
}
h2{
    color: #5d86b4;
    font-weight: 700 !important;
    font-size: 2.8rem !important;
    margin-bottom: 2% !important;
}
a{
    text-decoration: none;
}
.sidebar li {
    font-size: 1.2rem;
}
a, b, u, p, li, .text{
    font-size: 1.25rem;
    line-height: 1.8rem;
}
a, b, u, p, li, .text, button, .sidebar li{
    font-weight: 400;
}
h1, h2, a, b, u, p, li, .text, button, .sidebar li{
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
li::before {
    font-weight: bold;
    padding-right: 10px;
    margin-left: -3%;
    font-size: 2rem;
    color: #77AEDB;
    transition-duration: 0.5s;
}
li:hover::before {
    color: #337AB7;
}
button{
    border-radius: 30px !important;
    border: none !important;
    background: linear-gradient(to left, #a9d3dd, #9ba0cb);
    a{
        color:white;
        font-size: 1.48rem !important;
        font-weight: 400;
        text-decoration: none;
    }
}
#Advantages svg, #Services svg{
    width: 93%;
}
#Services svg{
    margin-top: -2%;
}
#About, #Services{
    li:before {
        content: "\25cb";
    }
    li:hover:before {
        content: "\25cf";
    }
}
#Advantages button, #Services button{
    width: 60%;
    margin: 1% 1.5%;
    padding: 1.5%;
}
#Home, #About, #Directions, #Advantages,
#Employees, #Services, #Contacts{
    padding: 2% 3% 2% 6%;
}
#Home{
    &:hover{
        #HeadPersonWithPapers1, #HeadPersonWithStick1,#Papers2,
        #RightHandPersonWithBook1, #HeadPersonWithBook2,#Hair2,
        #RightHandPersonWithStick2, #Stick2,#RightHandPersonWithRope1,
        #BagPersonWithRope2, #HeadPersonWithRope1, #Instruments2,
        #RightHandPersonWithTail1,#LeftHandPersonWithTail1, #LeftHandPersonWithBook1 {
            display: block;
            animation: up-down-1 3s infinite ;
        }

        #HeadPersonWithPapers2, #HeadPersonWithStick2,#Papers1,
        #RightHandPersonWithBook2,#HeadPersonWithBook1,#Hair1,
        #RightHandPersonWithStick1, #Stick1, #RightHandPersonWithRope2,
        #BagPersonWithRope1, #HeadPersonWithRope2, #Instruments1,
        #RightHandPersonWithTail2,#LeftHandPersonWithTail2, #LeftHandPersonWithBook2 {
            animation: up-down-2 3s infinite ;
        }
        @keyframes up-down-2 {
            from {
                visibility:hidden;
            }
            50% {
                visibility:hidden;
            }
            to {
                visibility:visible;
            }
        }
        @keyframes up-down-1{
            from {

                visibility:visible;
            }
            50% {
                visibility:hidden;
            }
            to {
                visibility:hidden;
            }
        }
    }
    #HeadPersonWithPapers1, #HeadPersonWithStick1,#Papers2,
    #RightHandPersonWithBook1, #HeadPersonWithBook2,#Hair2,
    #RightHandPersonWithStick2, #Stick2,#RightHandPersonWithRope1,
    #BagPersonWithRope2, #HeadPersonWithRope1, #Instruments2,
    #RightHandPersonWithTail1,#LeftHandPersonWithTail1, #LeftHandPersonWithBook1{
        display: none;
    }
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
        margin-top: 3%;
    }
    li{
        margin-bottom: 0;
    }
    svg{
        width: 100%;
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
        font-family: "Font Awesome 6 brands";
        content: "\2727";
    }
    li:hover:before {
        content: "\2726";
    }
}
#Advantages{
    ul li:before {
        font-family: "Font Awesome 6 brands";
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
    li:before {
        content: "\2606";
    }
    li:hover:before {
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
#Contacts{
    padding-bottom: 5%;
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
        width: 114%;
    }
    .nameContact{
        padding: 1%;
        svg{
            width: 2.35rem;
            margin-left: 2%;
            margin-top: 15%;
        }
    }
}
@media screen and (max-width: 992px){
    .sidebar.open {
        width: 100%;
    }
    #Home, #About, #Directions, #Advantages, #Employees, #Services, #Contacts {
        padding: 2% 3% 2% 3%;
    }
    #Home{
        .row{
            flex-direction: column;
        }
        .col-5{
            width: 100%;
            button{
                display: none;
            }
        }
        svg{
            margin: 0 auto;
            display: block;
        }
    }
    #About .row, #Employees .row, #Contacts .row{
        flex-direction: column-reverse;
    }
    #Advantages .row, #Services .row{
        flex-direction: column;
    }
    #Directions{
        .row{
            flex-direction: column;
        }
        .col{
            padding: 0 15px !important;
        }
    }
    #About, #Advantages, #Employees, #Services, #Contacts{
        .col-4, .col-5{
            width: 100%;
        }
        svg{
            margin: 3% auto 0;
            display: block;
        }
    }
    h1{
        width: 100%;
        margin-bottom: 0 !important;
        margin-top: 3% !important;
    }
    p{
        margin-bottom: .5rem !important;
    }
    ul{
        margin-bottom: 0 !important;
    }
    li {
        margin-bottom: 1%;
    }
    #Contacts .nameContact .row{
        flex-direction: inherit;
    }
}
@media screen and (max-width: 500px){
    body{
        padding-left: 45px;
    }
    .sidebar {
        width: 45px;
        #my-scroll {
            margin: 6px 0 0;
        }
        .logo-details{
            margin: 6px 0 0 75%;
            .bx-menu:before {
                margin-left: 8%;
            }
        }
        li i {
            font-size: 1.4rem;
        }
    }
    #Home, #About, #Directions, #Advantages, #Employees, #Services, #Contacts {
        padding: 2% !important;
    }
    #About svg, #Advantages svg, #Employees svg, #Services svg, #Contacts svg{
        width: 56%;
    }
    #Home{
        p{
            margin: 0 0 4%;
            font-size: 1rem;
            line-height: 1.6rem;
        }
        svg{
            width: 96%;
        }
    }
    h1{
        font-size: 1.45rem !important;
        line-height: 2rem !important;
    }
    h2{
        font-size: 1.25rem !important;
    }
    a, b, u, p, li, .text{
        font-size: 1rem;
        line-height: 1.2rem;
    }
    button a{
        font-size: 1.1rem !important;
    }
    li:before {
        margin-left: -3%;
        font-size: 1.1rem;
    }
    #Directions li:before {
        margin-left: -5%;
        font-size: 1.4rem;
    }
    ul{
        margin-left: -8%;
    }
    #Advantages button, #Services button {
        width: 90%;
    }
    #Contacts{
        .nameContact svg{
            width: 1.9rem;
            margin-left: -50%;
            margin-top: 75%;
        }
        .contacts {
            margin-left: 0;
        }
    }
}
@media screen and (min-width: 500px) and (max-width: 768px){
    #About svg, #Advantages svg, #Employees svg, #Services svg, #Contacts svg{
        width: 56%;
    }
    li:before {
        margin-left: 0;
        font-size: 1.1rem;
    }
    #Directions li:before {
        margin-left: -1%;
        font-size: 1.4rem;
    }
    #Home{
        p{
            margin: 0 0 4%;
            font-size: 1.2rem;
            line-height: 1.6rem;
        }
        svg{
            width: 96%;
        }
    }
    h1{
        font-size: 2.4rem !important;
        line-height: 2.3rem !important;
    }
    h2{
        font-size: 1.7rem !important;
    }
    ul{
        margin-left: -6%;
    }
    a, b, u, p, li, .text{
        font-size: 1.2rem;
        line-height: 1.4rem;
    }
    button a{
        font-size: 1.25rem !important;
    }
    #Advantages button, #Services button {
        width: 90%;
    }
    #Contacts{
        .nameContact svg{
            width: 1.9rem;
            margin-left: -50%;
            margin-top: 75%;
        }
        .contacts {
            margin-left: 0;
        }
    }
}
@media screen and (min-width: 768px) and (max-width: 992px){
    #About svg, #Advantages svg, #Employees svg, #Services svg, #Contacts svg{
        width: 48%;
    }
    #Home{
        p{
            margin: 0 0 4%;
            font-size: 1.2rem;
            line-height: 1.6rem;
        }
        svg{
            width: 66%;
        }
    }
    h1{
        font-size: 2.65rem !important;
        line-height: 2.35rem !important;
    }
    h2{
        font-size: 1.7rem !important;
    }
    ul{
        margin-left: -2%;
    }
    a, b, u, p, li, .text{
        font-size: 1.2rem;
        line-height: 1.4rem;
    }
    button a{
        font-size: 1.25rem !important;
    }
    #Contacts .nameContact svg{
        width: 2rem;
    }
}
@media screen and (min-width: 992px) and (max-width: 1200px){
    #Home, #About, #Directions, #Advantages, #Employees, #Services, #Contacts {
        padding: 2% 3% 2% 3%;
    }
    #About .row, #Employees .row, #Contacts .row{
        flex-direction: column-reverse;
    }
    #Advantages .row, #Services .row{
        flex-direction: column;
    }
    #Directions{
        .row{
            flex-direction: column;
        }
        .col{
            padding: 0 15px !important;
        }
    }
    #About, #Advantages, #Employees, #Services, #Contacts{
        .col-4, .col-5{
            width: 100%;
        }
        svg{
            margin: 3% auto 0;
            display: block;
            width: 45%;
        }
    }
    #Home{
        p{
            width: 106%;
            margin: 0 0 4%;
            font-size: 1.2rem;
            line-height: 1.6rem;
        }
        svg{
            margin-top: 2%;
            width: 124%;
            margin-left: -19%;
        }
    }
    h1{
        margin-top: 3% !important;
        font-size: 2.28rem !important;
        line-height: 2.8rem !important;
        margin-bottom: 0 !important;
    }
    h2{
        font-size: 2rem !important;
    }
    p{
        margin-bottom: .5rem !important;
    }
    a, b, u, p, li, .text{
        font-size: 1.2rem;
        line-height: 1.4rem;
    }
    ul{
        margin-left: -2%;
        margin-bottom: 0 !important;
    }
    li {
        margin-bottom: 1%;
    }
    button a{
        font-size: 1.25rem !important;
    }
    #Contacts .nameContact{
        svg{
            width: 2rem;
        }
        .row{
            flex-direction: inherit;
        }
    }
}
@media screen and (min-width: 1200px) and (max-width: 1400px){
    #Advantages svg, #Services svg{
        width: 95%;
    }
    #Home svg{
        width: 110%;
        margin-left: -8%;
    }
    #About svg{
        margin-left: -5%;
        width: 105%;
    }
    #Employees svg, #Contacts svg {
        margin-left: -12%;
        width: 110%;
    }
    h1{
        font-size: 2.65rem !important;
        line-height: 3.5rem !important;
        margin-bottom: 0 !important;
    }
    #Home p{
        margin: 0 0 4%;
        font-size: 1.2rem;
        line-height: 1.6rem;
    }
    h2{
        font-size: 2.15rem !important;
    }
    p{
        margin-bottom: .5rem !important;
    }
    a, b, u, p, li, .text{
        font-size: 1.2rem;
        line-height: 1.4rem;
    }
    ul{
        margin-left: -4%;
    }
    li {
        margin-bottom: 2%;
    }
    button a{
        font-size: 1.25rem !important;
    }
    #Contacts .nameContact svg{
        width: 2rem;
    }
}
@media screen and (min-width: 1400px) and (max-width: 1600px){
    h1{
        font-size: 3.5rem !important;
        line-height: 4.25rem !important;
    }
    #Home p{
        font-size: 1.35rem;
        line-height: 1.9rem;
    }
    h2{
        font-size: 2.6rem !important;
    }
    a, b, u, p, li, .text{
        font-size: 1.2rem;
        line-height: 1.45rem;
    }
    button a{
        font-size: 1.3rem !important;
    }
    #Contacts .nameContact svg{
        width: 2.15rem;
    }
}
</style>
