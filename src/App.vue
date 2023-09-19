<template>
  <div id="app">
      <navbar/>
      <Home/>
      <About/>
      <Directions/>
      <Advantages/>
      <Licenses/>
      <Employees/>
      <Services/>
      <Contacts/>
  </div>
</template>

<script>
    import Navbar from "@/components/Navbar";
    import Home from './components/Home.vue'
    import About from "@/components/About";
    import Advantages from "@/components/Advantages";
    import Employees from "@/components/Employees";
    import Services from "@/components/Services";
    import Contacts from "@/components/Contacts";
    import Directions from "@/components/Directions";
    import Licenses from "@/components/Licenses";

export default {
  name: 'App',
  components: {
      Navbar,
      Licenses,
      Directions,
      Contacts,
      Services,
      Employees,
      Advantages,
      About,
      Home,
  }
}
</script>

<style>
    @import "components/styleSvg/animationsSvg.scss";

    .modal-open {
        overflow: hidden;
    }
    .modal-footer {display: none !important;}
    /*заголовок модального окна*/
    .modal-header{
        padding: 0 0.5rem !important;
        background: linear-gradient(to left, #deedf0, #dcdeee);
    }
    /*тело модального окна*/
    .modal-body{
        padding: 0;
    }
    @media screen and (max-width: 500px) {
        /*"крестик" - кнопка закрытия модального окна*/
        .modal-header .close {
            padding: 0.5rem 0.5rem !important;
        }
    }
</style>
<style lang="scss">
body{
    background: #f2f4f6!important;
}
#Home, #Directions, #Licenses, #Services{
    background: #f2f4f6;

}
#About, #Advantages, #Employees, #Contacts{
    background: #e9f0f4;
}
#app{
    background: #e9f0f4 !important;
    height: 100%;
    margin: 0 !important;
    padding: 0 !important;
}
/*контейнер на блоки посередине экрана*/
.container{
    padding-right: 15px !important;
    padding-left: 15px !important;
}
/*картинки на всем сайте*/
img{
    width: 100%;
    height: auto;
}
h1{
    margin-top: 5px !important;
    font-size: 5.2rem !important;
    color: #5595d9;
    letter-spacing: -.5px;
    margin-left: -8px;
    margin-bottom: 0 !important;
    font-weight: 500 !important;
    line-height: 7rem !important;
    width: 135%;
    font-family: 'Roboto Condensed', sans-serif;
    text-shadow:  #4884c0 2px 1px 1px;
}
h2{
    font-weight: 500 !important;
    margin-top: 0 !important;
    font-size: 2.5rem !important;
    margin-bottom: 3% !important;
    font-family: 'Roboto Condensed', sans-serif;
    color: #5595d9;
    text-shadow:  #4884c0 1px .5px .5px;
    letter-spacing: -.5px;
}
a{
    text-decoration: none !important;
    color: black !important;
    &:hover{
        cursor: pointer;
    }
}
iframe{
    height: 82vh;
}
a, b, u, p, li, .text{
    font-size: 1.4rem;
    line-height: 1.85rem;
}
a, b, u, p, li, .text, button{
    font-weight: 400;
}
a, b, u, p, li, .text, button{
    font-weight: 400;
    font-family: 'Tinos', serif;
  }
ul{
    list-style: none !important;
    margin-bottom: 1.5% !important;
}
li{
    margin-bottom: 2.25%;
}
li::before{
    font-weight: bold;
    padding-right: 10px;
    margin-left: -3%;
    font-size: 1.5rem;
    color: #77AEDB;
    transition-duration: 0.5s;
}
li:hover::before{
    color: #337AB7;
}
button, #Home button{
    border: none !important;
    background: #f7f7f7;
    font-size: 1.5rem;
    &:hover{
        transform: scale(1.03);
    }
    a{
        color:black;
        font-weight: 400;
        text-decoration: none;
    }
}
.modal{
    button{
        background: transparent !important;
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
#Home{
    padding: 40px 0 110px 0;
}
#About, #Directions, #Advantages, #Licenses,
#Employees, #Services, #Contacts{
    padding: 80px 50px 80px;
}
.flex-container{
    display: flex;
    flex-wrap: wrap;
}
#Home{
    p{
        margin: 20px 0;
        font-size: 1.5rem;
        line-height: 2rem;
        width: 115%;
        font-weight: 500;
    }
    h2{
        color: #5e6571;
        width: 115%;
        font-weight: 500 !important;
        margin: 3% 0 !important;
        font-family: 'Marck Script', cursive;
    }
    .buttonGroup{
        width: 115%;
        margin-left: -15px;
    }
    button{
        width: 46%;
        float: left;
        background: #d1ebff;
        border-radius: 25px;
        margin: 4% 0;
        padding: 10px;
        &:last-child{
            margin-left: 4% !important;
            background: transparent;
            border: 2px solid #bfdbf1 !important;
        }
    }
    svg{
        margin-top: -20px;
        width: 100%;
        margin-left: 50px;
    }
}
#About{
    .row{
        margin: 15px 0;
    }
    li, ul{
        margin-bottom: 0 !important;
    }
    svg{
        width: 150%;
        margin-top: 10%;
        margin-left: -20%;
    }
    .col{
        padding-left: 7%;
    }
}
#Directions{
    .col{
        padding: 0 !important;
        div{
            padding: 20px 0 5px;
            background: #f2f4f6;
            margin: 2% 3%;
            box-shadow: 0 2px 18px rgba(41, 41, 41, 0.1);
        }
    }
    svg{
        margin: 0 auto;
        width: 90%;
        display: block;
    }
    .wrapper {
        display: flex;
        flex-wrap: wrap;
        box-shadow: none !important;
        div{
            width: 100%;
            margin: 0 auto 1%;
            box-shadow: none;
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
    h2{
        margin-top: 6% !important;
    }
    ul li:before {
        content: "\2713";
    }
    li{
        margin-bottom: 3%;
    }
    svg{
        width: 100%;
        padding: 0;
    }
}
#Licenses{
    h2{
        text-align: center;
    }
    a:hover{
        color: #0766ce !important;
    }
    table{
        border-color: #b0cde2 !important;
        tr td:first-child{
            width: 61%;
        }
        svg{
            width: 23px;
            float: left;
        }
    }
    span{
        float: left;
        padding: 0 10px;
    }
    svg{
        width: 100%;
        padding: 0;
    }
}
#Employees{
    .employee{
        width: 46%;
        height: 180px;
        margin: 8px 15px;
        span{
            font-weight: 600;
        }
        .row{
            margin-top: 4%;
        }
    }
    svg{
        padding: 0;
        width: 100%;
        margin-top: -1.5%;
    }
    .svgEmployees{
        margin: 8px 15px;
        width: 46%;
        height: 180px;
    }
}
#Employees .employee, #Contacts .contacts{
    padding: 10px;
    box-shadow: 0px 2px 18px rgba(41, 41, 41, 0.1);
    background: #f2f4f6;
}
#Services{
    svg{
        width: 108%;
        padding: 0;
        margin-left: -8%;
        margin-top: -20px;
    }
    button{
        width: 60%;
        margin: 3% 1.5% 0;
        padding: 2% 2.5%;
        background: #d1ebff;
        border-radius: 25px;
        box-shadow: 0 1px 2px rgba(41, 41, 41, 0.1);
        color: black;

    }
}
#Contacts{
    .contacts{
        margin: 20px;
        .row{
            padding: 10px;
            b{
                display: block;
                margin-bottom: 10px;
            }
            svg{
                margin-top: 5%;
                margin-left: -8%;
                padding: 10px;
                width: 100%;
            }
        }
    }
}
@media screen and (max-width: 992px){
    #Home{
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
}
@media screen and (max-width: 500px){
    #Home, #About, #Directions,
    #Licenses, #Advantages, #Employees,
    #Services, #Contacts {
        padding: 25px 3% 25px 3%;
    }
    h1{
        text-align: center;
        margin-top: 0 !important;
        font-size: 2rem !important;
        line-height: 3rem !important;
    }
    h2{
        font-size: 1.7rem !important;
    }
    a, b, u, p, li, .text, #Home p{
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
    #About li, #About ul{
        margin-left: -4%;
    }
    ul{
        margin-left: -3%;
    }
    #Home{
        p{
            margin: 0 0 4%;
            width: 100%;
            text-align: center;
        }
        svg{
            width: 90%;
        }
        h2{
            width: 100%;
            text-align: center;
            font-size: 1.4rem !important;
        }
    }
    #About {
        .row {
            flex-direction: column-reverse;
        }
        .col {
            padding-left: 0;
        }
        .col-3 {
            width: 100%;
        }
        svg {
            width: 65%;
            margin-left: 17.5%;
            margin-top: 0;
        }
    }
    #Directions{
        .row{
            flex-direction: column;
        }
        .col div{
            padding: 0;
        }
        svg {
            width: 60%;
        }
    }
    #Advantages{
        h2{
            margin-top: 0;
        }
        .row{
            flex-direction: column;
        }
        .col-5 {
            width: 100%;
        }
        svg {
            width: 60%;
            margin-left: 20%;
            margin-top: 0;
        }
    }
    #Licenses{
        .table > :not(caption) > * > *{
            padding: 0.35rem 0.35rem !important;
        }
        table  tr td:first-child{
            width: 78%;
        }
        table svg{
            margin-left: 0;
        }
        table span{
            display: none;
        }
        .row{
            flex-direction: column-reverse;
        }
        .col-5 {
            width: 100%;
        }
        svg {
            width: 60%;
            margin-left: 25%;
            margin-top: 0;
        }
    }
    #Employees{
        .employee {
            padding: 15px;
            height: 140px;
            width: 100%;
            .row {
                margin-top: 2%;
                svg{
                    width: 130%;
                    margin-left: -15%;
                }
            }
        }
        .svgEmployees {
            margin: 2% auto 0;
            width: 80%;
            height: 90px;
        }
    }
    #Services{
        .row{
            flex-direction: column-reverse;
        }
        button{
            width: 100%;
            margin-bottom: 5%;
        }
        .col-5 {
            width: 100%;
        }
        svg {
            width: 65%;
            margin-left: 17.5%;
            margin-top: 0;
        }
    }
    #Contacts{
        .row{
            flex-direction: column;
            .row{
                flex-direction: row;
                .col{
                    margin-left: -15%;
                }
            }
        }
        .contacts {
            padding: 0;
            margin: 0 0 2%;
            .row svg {
                margin-top: 0;
                width: 50%;
                padding: 3px;
            }
        }
    }
}
@media screen and (min-width: 500px) and (max-width: 768px){
    #Home{
        padding: 0 0 60px 0;
    }
    #About, #Directions, #Licenses,
    #Advantages, #Licenses, #Employees,
    #Services, #Contacts{
        padding: 40px 30px 40px;
    }
    li:before {
        margin-left: 0;
        font-size: 1.1rem;
    }
    #Home{
        p{
            margin: 2% 0 4%;
            width: 100%;
            text-align: center;
        }
        svg{
            width: 78%;
        }
        h2{
            width: 100%;
            text-align: center;
        }
    }
    #About {
        .row {
            flex-direction: column-reverse;
        }
        .col {
            padding-left: 0;
        }
        .col-3 {
            width: 100%;
        }
        svg {
            width: 55%;
            margin-left: 22.5%;
            margin-top: 0;
        }
    }
    #Directions{
        .row{
            flex-direction: column;
        }
        .col div{
            padding: 0;
        }
        svg {
            width: 50%;
        }
    }
    #Advantages{
        h2{
            margin-top: 0 !important;
        }
        .row{
            flex-direction: column;
        }
        .col-5 {
            width: 100%;
        }
        svg {
            width: 50%;
            margin-left: 25%;
            margin-top: 0;
        }
    }
    #Licenses{
        .table > :not(caption) > * > *{
            padding: 0.35rem 0.35rem !important;
        }
        table  tr td:first-child{
            width: 78%;
        }
        table svg{
            margin-left: 0;
        }
        table span{
            display: none;
        }
        .row{
            flex-direction: column-reverse;
        }
        .col-5 {
            width: 100%;
        }
        svg {
            width: 50%;
            margin-left: 25%;
            margin-top: 0;
        }
    }
    #Employees{
        .employee {
            padding: 15px;
            height: 150px;
            width: 100%;
            margin: 8px 0;
            .row {
                margin-top: 2%;
            }
        }
        .svgEmployees {
            margin: 0 auto;
            width: 80%;
            height: 150px;
        }
    }
    #Services{
        .row{
            flex-direction: column-reverse;
        }
        button{
            width: 100%;
            margin-bottom: 5%;
        }
        .col-5 {
            width: 100%;
        }
        svg {
            width: 50%;
            margin-left: 25%;
            margin-top: 0;
        }
    }
    #Contacts{
        .row{
            flex-direction: column;
            .row{
                flex-direction: row;
                .col{
                    margin-left: -12%;
                }
            }
        }
        .contacts {
            padding: 5px;
            margin: 0 0 2%;
            .row svg {
                padding: 5px;
                margin-top: 0;
                width: 50%;
            }
        }
    }
    h1{
        text-align: center;
        margin-top: 0 !important;
        font-size: 2.6rem !important;
        line-height: 3rem !important;
    }
    h2{
        font-size: 1.9rem !important;
    }
    #About li, #About ul{
        margin-left: -6%;
    }
    ul{
        margin-left: -3%;
    }
    a, b, u, p, li, .text, #Home p{
        font-size: 1.2rem;
        line-height: 1.4rem;
    }
    button a{
        font-size: 1.25rem !important;
    }
}
@media screen and (min-width: 768px) and (max-width: 992px){
    #Home{
        padding: 0 0 60px 0;
    }
    #About, #Directions, #Advantages, #Licenses,
    #Employees, #Services, #Contacts{
        padding: 40px 30px 40px;
    }
    #Home{
        p{
            margin: 0 auto 4%;
            width: 100%;
            text-align: center;
        }
        svg{
            width: 66%;
        }
        h2{
            width: 100%;
            text-align: center;
        }
    }
    #About {
        .row {
            flex-direction: column-reverse;
        }
        .col {
            padding-left: 0;
        }
        .col-3 {
            width: 100%;
        }
        svg {
            width: 55%;
            margin-left: 22.5%;
            margin-top: 0;
        }
    }
    #Directions{
        .row{
            flex-direction: column;
        }
        .col div{
            padding: 0;
        }
        svg {
            width: 50%;
        }
    }
    #Advantages{
        h2{
            margin-top: 0 !important;
        }
        .row{
            flex-direction: column;
        }
        .col-5 {
            width: 100%;
        }
        svg {
            width: 50%;
            margin-left: 25%;
            margin-top: 0;
        }
    }
    #Licenses{
        .table > :not(caption) > * > *{
            padding: 0.5rem 0.35rem !important;
        }
        table  tr td:first-child{
            width: 80%;
        }
        table svg{
            margin-left: 0;
        }
        table span{
            display: none;
        }
        .row{
            flex-direction: column-reverse;
        }
        .col-5 {
            width: 100%;
        }
        svg {
            width: 50%;
            margin-left: 25%;
            margin-top: 0;
        }
    }
    #Employees{
        .employee {
            padding: 15px;
            height: 150px;
            width: 100%;
            margin: 8px 0;
            .row {
                margin-top: 2%;
            }
        }
        .svgEmployees {
            margin: 0 auto;
            width: 80%;
            height: 150px;
        }
    }
    #Services{
        .row{
            flex-direction: column-reverse;
        }
        button{
            width: 100%;
            margin-bottom: 5%;
        }
        .col-5 {
            width: 100%;
        }
        svg {
            width: 50%;
            margin-left: 25%;
            margin-top: 0;
        }
    }
    #Contacts{
        .row{
            flex-direction: column;
            .row{
                flex-direction: row;
                .col{
                    margin-left: -12%;
                }
            }
        }
        .contacts {
            margin: 0 0 2%;
            .row svg {
                margin-top: 0;
                width: 50%;
            }
        }
    }
    h1{
        text-align: center;
        margin-top: 0 !important;
        font-size: 3rem !important;
        line-height: 5rem !important;
    }
    h2{
        font-size: 2rem !important;
    }
    ul, #About li, #About ul{
        margin-left: -2%;
    }
    a, b, u, p, li, .text, #Home p{
        font-size: 1.2rem;
        line-height: 1.4rem;
    }
    button a{
        font-size: 1.25rem !important;
    }
}
@media screen and (min-width: 992px) and (max-width: 1200px){
    #Home{
        padding: 30px 0 60px 0;
    }
    #About, #Directions, #Advantages, #Licenses,
    #Employees, #Services, #Contacts{
        padding: 40px 30px 40px;
    }
    #Home{
        p{
            width: 106%;
            margin: 0 0 4%;
        }
        svg{
            width: 94%;
            margin-left: 30px;
        }
        h2{
            font-size: 1.8rem !important;
        }
    }
    #Advantages h2 {
        margin-top: 3% !important;
    }
    #Licenses{
        svg{
            margin-top: 25%;
        }
        .col{
            padding-left: 0 !important;
            svg{
                margin: 0;
            }
        }
        .table > :not(caption) > * > *{
           padding: 0.35rem 0.35rem !important;
        }
        table  tr td:first-child{
            width: 49%;
        }
    }
    #Employees .svgEmployees{
        margin: 46px 15px 8px;
    }
    #Contacts{
        .contacts {
            margin: 10px;
            padding: 5px;
            .row svg {
                padding: 5px;
            }
        }
    }
    h1{
        margin-top: 3% !important;
        font-size: 3.5rem !important;
        line-height: 4.5rem !important;
        margin-bottom: 0 !important;
    }
    h2{
        font-size: 2rem !important;
    }
    p{
        margin-bottom: .5rem !important;
    }
    a, b, u, p, li, .text, #Home p{
        font-size: 1.2rem;
        line-height: 1.4rem;
    }
    button, #Home button{
        font-size: 1.25rem !important;
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
}
@media screen and (min-width: 1200px) and (max-width: 1400px){
    #Advantages svg, #Services svg{
        width: 95%;
    }
    h1{
        font-size: 4rem !important;
        line-height: 5rem !important;
        margin-bottom: 0 !important;
    }
    button, #Home button{
        font-size: 1.25rem !important;
    }
    #Home{
        svg{
            width: 94%;
            margin-left: 50px;
        }
        h2{
            font-size: 2rem !important;
        }
    }
    #Licenses table  tr td:first-child{
        width: 55%;
    }
    #Contacts .contacts .row svg {
        padding: 5px;
    }
    h2{
        font-size: 2.5rem !important;
    }
    p{
        margin-bottom: .5rem !important;
    }
    a, b, u, p, li, .text, #Home p{
        font-size: 1.22rem;
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
}
</style>
