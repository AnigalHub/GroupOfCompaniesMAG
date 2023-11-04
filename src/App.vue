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
    /*футер модального окна*/
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
#app{
    background: #e9f0f4 !important;
    height: 100%;
    margin: 0 !important;
    padding: 0 !important;
}
/*компоненты - Главная, Направления, Лицензии, Услуги*/
#Home, #Directions, #Licenses, #Services{
    background: #f2f4f6;
}
/*компоненты - О нас, Преимущества, Сотрудники, Контакты*/
#About, #Advantages, #Employees, #Contacts{
    background: #e9f0f4;
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
/*заголовки*/
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
/*ссылки*/
a{
    text-decoration: none !important;
    color: black !important;
    /*при наведении*/
    &:hover{
        cursor: pointer;
    }
}
/*фрейм для документов*/
iframe{
    height: 82vh;
}
/*ссылки, жирный текст, список, параграф, пункты списка, текст*/
a, b, u, p, li, .text{
    font-size: 1.4rem;
    line-height: 1.85rem;
}
/*ссылки, жирный текст, список, параграф, пункты списка, текст, кнопки*/
a, b, u, p, li, .text, button{
    font-weight: 400;
    font-weight: 400;
    font-family: 'Tinos', serif;
}
/*список*/
ul{
    list-style: none !important;
    margin-bottom: 1.5% !important;
}
/*пункты списка*/
li{
    margin-bottom: 2.25%;
}
/*пункты списка(до, пункты)*/
li::before{
    font-weight: bold;
    padding-right: 10px;
    margin-left: -3%;
    font-size: 1.5rem;
    color: #77AEDB;
    transition-duration: 0.5s;
}
/*пункты списка - при наведении(до, пункты)*/
li:hover::before{
    color: #337AB7;
}
/*кнопки, компонент - Главная (кнопки)*/
button, #Home button{
    border: none !important;
    background: #f7f7f7;
    font-size: 1.5rem;
    /*при наведении*/
    &:hover{
        transform: scale(1.03);
    }
    /*ссылки*/
    a{
        color:black;
        font-weight: 400;
        text-decoration: none;
    }
}
/*модальное окно*/
.modal{
    /*кнопки*/
    button{
        background: transparent !important;
    }
}
/*компоненты - О нас, Услуги*/
#About, #Services{
    /*пункты списка(до, пункты)*/
    li:before {
        content: "\25cb";
    }
    /*пункты списка - при наведении(до, пункты)*/
    li:hover:before {
        content: "\25cf";
    }
}
/*компоненты - Главная*/
#Home{
    padding: 40px 0 110px 0;
}
/*компоненты - Главная, Направления, Преимущества, Лицензии, Сотрудники, Услуги, Контакты*/
#About, #Directions, #Advantages, #Licenses, #Employees, #Services, #Contacts{
    padding: 80px 50px 80px;
}
/*контейнер, который включает в себя повтор блоков*/
.flex-container{
    display: flex;
    flex-wrap: wrap;
}
/*компоненты - Главная*/
#Home{
    /*параграф*/
    p{
        margin: 20px 0;
        font-size: 1.5rem;
        line-height: 2rem;
        width: 115%;
        font-weight: 500;
    }
    /*заголовки*/
    h2{
        color: #5e6571;
        width: 115%;
        font-weight: 500 !important;
        margin: 3% 0 !important;
        font-family: 'Marck Script', cursive;
    }
    /*блок под кнопки*/
    .buttonGroup{
        width: 115%;
        margin-left: -15px;
    }
    /*кнопки*/
    button{
        width: 46%;
        float: left;
        background: #d1ebff;
        border-radius: 25px;
        margin: 4% 0;
        padding: 10px;
        /*последняя*/
        &:last-child{
            margin-left: 4% !important;
            background: transparent;
            border: 2px solid #bfdbf1 !important;
        }
    }
    /*svg*/
    svg{
        margin-top: -20px;
        width: 100%;
        margin-left: 50px;
    }
}
/*компоненты - О нас*/
#About{
    /*бутстрап сетка*/
    .row{
        margin: 15px 0;
    }
    /*список, пункты списка*/
    li, ul{
        margin-bottom: 0 !important;
    }
    /*svg*/
    svg{
        width: 150%;
        margin-top: 10%;
        margin-left: -20%;
    }
    /*бутстрап сетка*/
    .col{
        padding-left: 7%;
    }
}
/*компоненты - Направления*/
#Directions{
    /*бутстрап сетка*/
    .col{
        padding: 0 !important;
        /*блок*/
        div{
            padding: 20px 0 5px;
            background: #f2f4f6;
            margin: 2% 3%;
            box-shadow: 0 2px 18px rgba(41, 41, 41, 0.1);
        }
    }
    /*svg*/
    svg{
        margin: 0 auto;
        width: 90%;
        display: block;
    }
    /*обертка блока*/
    .wrapper {
        display: flex;
        flex-wrap: wrap;
        box-shadow: none !important;
        /*блок*/
        div{
            width: 100%;
            margin: 0 auto 1%;
            box-shadow: none;
        }
    }
    /*пункты списка(до, пункты)*/
    li:before {
        content: "\2727";
    }
    /*пункты списка - при наведении(до, пункты)*/
    li:hover:before {
        content: "\2726";
    }
}
/*компоненты - Преимущества*/
#Advantages{
    /*заголовки*/
    h2{
        margin-top: 6% !important;
    }
    /*пункты списка(до, пункты)*/
    ul li:before {
        content: "\2713";
    }
    /*пункты списка*/
    li{
        margin-bottom: 3%;
    }
    /*svg*/
    svg{
        width: 100%;
        padding: 0;
    }
}
/*компоненты - Лицензии*/
#Licenses{
    /*заголовки*/
    h2{
        text-align: center;
    }
    /*ссылки при наведении*/
    a:hover{
        color: #0766ce !important;
    }
    /*таблица*/
    table{
        border-color: #b0cde2 !important;
        /*первый столбец таблицы*/
        tr td:first-child{
            width: 61%;
        }
        /*svg*/
        svg{
            width: 23px;
            float: left;
        }
    }
    /*выделение главного*/
    span{
        float: left;
        padding: 0 10px;
    }
    /*svg*/
    svg{
        width: 100%;
        padding: 0;
    }
}
/*компоненты - Сотрудники*/
#Employees{
    /*блоки под информацию о сотрудниках*/
    .employee{
        width: 46%;
        height: 180px;
        margin: 8px 15px;
        /*выделение главного*/
        span{
            font-weight: 600;
        }
        /*бутстрап сетка*/
        .row{
            margin-top: 4%;
        }
    }
    /*svg*/
    svg{
        padding: 0;
        width: 100%;
        margin-top: -1.5%;
    }
    /*блок под svg*/
    .svgEmployees{
        margin: 8px 15px;
        width: 46%;
        height: 180px;
    }
}
/*компоненты - Сотрудники (блоки под информацию о сотрудниках), Контакты (блоки под информацию о контактах)*/
#Employees .employee, #Contacts .contacts{
    padding: 10px;
    box-shadow: 0px 2px 18px rgba(41, 41, 41, 0.1);
    background: #f2f4f6;
}
/*компоненты - Услуги*/
#Services{
    /*svg*/
    svg{
        width: 108%;
        padding: 0;
        margin-left: -8%;
        margin-top: -20px;
    }
    /*кнопки*/
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
/*компоненты - Контакты*/
#Contacts{
    /*блоки под информацию о контактах*/
    .contacts{
        margin: 20px;
        /*бутстрап сетка*/
        .row{
            padding: 10px;
            /*жирный шрифт*/
            b{
                display: block;
                margin-bottom: 10px;
            }
            /*svg*/
            svg{
                margin-top: 5%;
                margin-left: -8%;
                padding: 10px;
                width: 100%;
            }
        }
    }
}

/*АДАПТИВНОСТЬ*/
@media screen and (max-width: 992px){
    /*компоненты - Главная*/
    #Home{
        /*бутстрап сетка*/
        .col-5{
            width: 100%;
            /*кнопки*/
            button{
                display: none;
            }
        }
        /*svg*/
        svg{
            margin: 0 auto;
            display: block;
        }
    }
    /*заголовки*/
    h1{
        width: 100%;
        margin-bottom: 0 !important;
        margin-top: 3% !important;
    }
    /*параграф*/
    p{
        margin-bottom: .5rem !important;
    }
    /*список*/
    ul{
        margin-bottom: 0 !important;
    }
    /*пункты списка*/
    li {
        margin-bottom: 1%;
    }
}
@media screen and (max-width: 500px){
    /*компоненты - Главная, Направления, Преимущества, Лицензии, Сотрудники, Услуги, Контакты*/
    #Home, #About, #Directions, #Licenses, #Advantages, #Employees, #Services, #Contacts {
        padding: 25px 3% 25px 3%;
    }
    /*заголовки*/
    h1{
        text-align: center;
        margin-top: 0 !important;
        font-size: 2rem !important;
        line-height: 3rem !important;
    }
    h2{
        font-size: 1.7rem !important;
    }
    /*ссылки, жирный текст, список, параграф, пункты списка, текст*/
    a, b, u, p, li, .text, #Home p{
        font-size: 1rem;
        line-height: 1.2rem;
    }
    /*ссылка в кнопке*/
    button a{
        font-size: 1.1rem !important;
    }
    /*пункты списка(до, пункты)*/
    li:before {
        margin-left: -3%;
        font-size: 1.1rem;
    }
    /*компонент - Направления (пункты списка(до, пункты))*/
    #Directions li:before {
        margin-left: -5%;
        font-size: 1.4rem;
    }
    /*компонент - О нас(список и пункты списка)*/
    #About li, #About ul{
        margin-left: -4%;
    }
    /*список*/
    ul{
        margin-left: -3%;
    }
    /*компонент - Главная*/
    #Home{
        /*параграф*/
        p{
            margin: 0 0 4%;
            width: 100%;
            text-align: center;
        }
        /*svg*/
        svg{
            width: 90%;
        }
        /*заголовки*/
        h2{
            width: 100%;
            text-align: center;
            font-size: 1.4rem !important;
        }
    }
    /*компонент - О нас*/
    #About{
        /*бутстрап сетка*/
        .row{
            flex-direction: column-reverse;
        }
        /*бутстрап сетка*/
        .col{
            padding-left: 0;
        }
        /*бутстрап сетка*/
        .col-3{
            width: 100%;
        }
        /*svg*/
        svg{
            width: 65%;
            margin-left: 17.5%;
            margin-top: 0;
        }
    }
    /*компонент - Направления*/
    #Directions{
        /*бутстрап сетка*/
        .row{
            flex-direction: column;
        }
        /*бутстрап сетка*/
        .col div{
            padding: 0;
        }
        /*svg*/
        svg{
            width: 60%;
        }
    }
    /*компонент - Преимущества*/
    #Advantages{
        /*заголовки*/
        h2{
            margin-top: 0;
        }
        /*бутстрап сетка*/
        .row{
            flex-direction: column;
        }
        /*бутстрап сетка*/
        .col-5 {
            width: 100%;
        }
        /*svg*/
        svg{
            width: 60%;
            margin-left: 20%;
            margin-top: 0;
        }
    }
    /*компонент - Лицензии*/
    #Licenses{
        /*отступы в таблице*/
        .table > :not(caption) > * > *{
            padding: 0.35rem 0.35rem !important;
        }
        /*первый столбец таблицы*/
        table  tr td:first-child{
            width: 78%;
        }
        /*svg в таблице*/
        table svg{
            margin-left: 0;
        }
        /*выделения важного в таблице*/
        table span{
            display: none;
        }
        /*бутстрап сетка*/
        .row{
            flex-direction: column-reverse;
        }
        /*бутстрап сетка*/
        .col-5{
            width: 100%;
        }
        /*svg*/
        svg{
            width: 60%;
            margin-left: 25%;
            margin-top: 0;
        }
    }
    /*компонент - Сотрудники*/
    #Employees{
        /*блоки под информацию о сотрудниках*/
        .employee{
            padding: 15px;
            height: 140px;
            width: 100%;
            /*бутстрап сетка*/
            .row{
                margin-top: 2%;
                /*svg*/
                svg{
                    width: 130%;
                    margin-left: -15%;
                }
            }
        }
        /*блок под svg*/
        .svgEmployees{
            margin: 2% auto 0;
            width: 80%;
            height: 90px;
        }
    }
    /*компонент - Услуги*/
    #Services{
        /*бутстрап сетка*/
        .row{
            flex-direction: column-reverse;
        }
        /*кнопки*/
        button{
            width: 100%;
            margin-bottom: 5%;
        }
        /*бутстрап сетка*/
        .col-5 {
            width: 100%;
        }
        /*svg*/
        svg{
            width: 65%;
            margin-left: 17.5%;
            margin-top: 0;
        }
    }
    /*компонент - Контакты*/
    #Contacts{
        /*бутстрап сетка*/
        .row{
            flex-direction: column;
            /*бутстрап сетка*/
            .row{
                flex-direction: row;
                /*бутстрап сетка*/
                .col{
                    margin-left: -15%;
                }
            }
        }
        /*блоки под информацию о контактах*/
        .contacts {
            padding: 0;
            margin: 0 0 2%;
            /*svg*/
            .row svg{
                margin-top: 0;
                width: 50%;
                padding: 3px;
            }
        }
    }
}
@media screen and (min-width: 500px) and (max-width: 768px){
    /*компоненты - Главная*/
    #Home{
        padding: 0 0 60px 0;
    }
    /*компоненты - Главная, Направления, Преимущества, Лицензии, Сотрудники, Услуги, Контакты*/
    #About, #Directions, #Licenses, #Advantages, #Licenses, #Employees, #Services, #Contacts{
        padding: 40px 30px 40px;
    }
    /*пункты списка(до, пункты)*/
    li:before {
        margin-left: 0;
        font-size: 1.1rem;
    }
    /*заголовки*/
    h1{
        text-align: center;
        margin-top: 0 !important;
        font-size: 2.6rem !important;
        line-height: 3rem !important;
    }
    h2{
        font-size: 1.9rem !important;
    }
    /*компонент - О нас(список и пункты списка)*/
    #About li, #About ul{
        margin-left: -6%;
    }
    /*список*/
    ul{
        margin-left: -3%;
    }
    /*ссылки, жирный текст, список, параграф, пункты списка, текст*/
    a, b, u, p, li, .text, #Home p{
        font-size: 1.2rem;
        line-height: 1.4rem;
    }
    /*ссылка в кнопке*/
    button a{
        font-size: 1.25rem !important;
    }
    /*компонент - Главная*/
    #Home{
        /*параграф*/
        p{
            margin: 2% 0 4%;
            width: 100%;
            text-align: center;
        }
        /*svg*/
        svg{
            width: 78%;
        }
        /*заголовки*/
        h2{
            width: 100%;
            text-align: center;
        }
    }
    /*компонент - О нас*/
    #About {
        /*бутстрап сетка*/
        .row{
            flex-direction: column-reverse;
        }
        /*бутстрап сетка*/
        .col{
            padding-left: 0;
        }
        /*бутстрап сетка*/
        .col-3{
            width: 100%;
        }
        /*svg*/
        svg{
            width: 55%;
            margin-left: 22.5%;
            margin-top: 0;
        }
    }
    /*компонент - Направления*/
    #Directions{
        /*бутстрап сетка*/
        .row{
            flex-direction: column;
        }
        /*бутстрап сетка*/
        .col div{
            padding: 0;
        }
        /*svg*/
        svg{
            width: 50%;
        }
    }
    /*компонент - Преимущества*/
    #Advantages{
        /*заголовки*/
        h2{
            margin-top: 0 !important;
        }
        /*бутстрап сетка*/
        .row{
            flex-direction: column;
        }
        /*бутстрап сетка*/
        .col-5 {
            width: 100%;
        }
        /*svg*/
        svg{
            width: 50%;
            margin-left: 25%;
            margin-top: 0;
        }
    }
    /*компонент - Лицензии*/
    #Licenses{
        /*отступы в таблице*/
        .table > :not(caption) > * > *{
            padding: 0.35rem 0.35rem !important;
        }
        /*первый столбец таблицы*/
        table tr td:first-child{
            width: 78%;
        }
        /*svg в таблице*/
        table svg{
            margin-left: 0;
        }
        /*выделения важного в таблице*/
        table span{
            display: none;
        }
        /*бутстрап сетка*/
        .row{
            flex-direction: column-reverse;
        }
        /*бутстрап сетка*/
        .col-5{
            width: 100%;
        }
        /*svg*/
        svg{
            width: 50%;
            margin-left: 25%;
            margin-top: 0;
        }
    }
    /*компонент - Сотрудники*/
    #Employees{
        /*блоки под информацию о сотрудниках*/
        .employee{
            padding: 15px;
            height: 150px;
            width: 100%;
            margin: 8px 0;
            /*бутстрап сетка*/
            .row{
                margin-top: 2%;
            }
        }
        /*блок под svg*/
        .svgEmployees{
            margin: 0 auto;
            width: 80%;
            height: 150px;
        }
    }
    /*компонент - Услуги*/
    #Services{
        /*бутстрап сетка*/
        .row{
            flex-direction: column-reverse;
        }
        /*кнопки*/
        button{
            width: 100%;
            margin-bottom: 5%;
        }
        /*бутстрап сетка*/
        .col-5{
            width: 100%;
        }
        /*svg*/
        svg{
            width: 50%;
            margin-left: 25%;
            margin-top: 0;
        }
    }
    /*компонент - Контакты*/
    #Contacts{
        /*бутстрап сетка*/
        .row{
            flex-direction: column;
            /*бутстрап сетка*/
            .row{
                flex-direction: row;
                /*бутстрап сетка*/
                .col{
                    margin-left: -12%;
                }
            }
        }
        /*блоки под информацию о контактах*/
        .contacts{
            padding: 5px;
            margin: 0 0 2%;
            /*svg*/
            .row svg{
                padding: 5px;
                margin-top: 0;
                width: 50%;
            }
        }
    }
}
@media screen and (min-width: 768px) and (max-width: 992px){
    /*компонент - Главная*/
    #Home{
        padding: 0 0 60px 0;
    }
    /*компоненты - Направления, Преимущества, Лицензии, Сотрудники, Услуги, Контакты*/
    #About, #Directions, #Advantages, #Licenses, #Employees, #Services, #Contacts{
        padding: 40px 30px 40px;
    }
    /*заголовки*/
    h1{
        text-align: center;
        margin-top: 0 !important;
        font-size: 3rem !important;
        line-height: 5rem !important;
    }
    h2{
        font-size: 2rem !important;
    }
    /*компонент - О нас(список и пункты списка)*/
    ul, #About li, #About ul{
        margin-left: -2%;
    }
    /*ссылки, жирный текст, список, параграф, пункты списка, текст*/
    a, b, u, p, li, .text, #Home p{
        font-size: 1.2rem;
        line-height: 1.4rem;
    }
    /*ссылка в кнопке*/
    button a{
        font-size: 1.25rem !important;
    }
    /*компонент - Главная*/
    #Home{
        /*параграф*/
        p{
            margin: 0 auto 4%;
            width: 100%;
            text-align: center;
        }
        /*svg*/
        svg{
            width: 66%;
        }
        /*заголовки*/
        h2{
            width: 100%;
            text-align: center;
        }
    }
    /*компонент - О нас*/
    #About{
        /*бутстрап сетка*/
        .row{
            flex-direction: column-reverse;
        }
        /*бутстрап сетка*/
        .col{
            padding-left: 0;
        }
        /*бутстрап сетка*/
        .col-3{
            width: 100%;
        }
        /*svg*/
        svg{
            width: 55%;
            margin-left: 22.5%;
            margin-top: 0;
        }
    }
    /*компонент - Направления*/
    #Directions{
        /*бутстрап сетка*/
        .row{
            flex-direction: column;
        }
        /*бутстрап сетка*/
        .col div{
            padding: 0;
        }
        /*svg*/
        svg{
            width: 50%;
        }
    }
    /*компонент - Преимущества*/
    #Advantages{
        /*заголовки*/
        h2{
            margin-top: 0 !important;
        }
        /*бутстрап сетка*/
        .row{
            flex-direction: column;
        }
        /*бутстрап сетка*/
        .col-5{
            width: 100%;
        }
        /*svg*/
        svg{
            width: 50%;
            margin-left: 25%;
            margin-top: 0;
        }
    }
    /*компонент - Лицензии*/
    #Licenses{
        /*отступы в таблице*/
        .table > :not(caption) > * > *{
            padding: 0.5rem 0.35rem !important;
        }
        /*первый столбец таблицы*/
        table tr td:first-child{
            width: 80%;
        }
        /*svg в таблице*/
        table svg{
            margin-left: 0;
        }
        /*выделения важного в таблице*/
        table span{
            display: none;
        }
        /*бутстрап сетка*/
        .row{
            flex-direction: column-reverse;
        }
        /*бутстрап сетка*/
        .col-5{
            width: 100%;
        }
        /*svg*/
        svg{
            width: 50%;
            margin-left: 25%;
            margin-top: 0;
        }
    }
    /*компонент - Сотрудники*/
    #Employees{
        /*блоки под информацию о сотрудниках*/
        .employee{
            padding: 15px;
            height: 150px;
            width: 100%;
            margin: 8px 0;
            /*бутстрап сетка*/
            .row{
                margin-top: 2%;
            }
        }
        /*блок под svg*/
        .svgEmployees {
            margin: 0 auto;
            width: 80%;
            height: 150px;
        }
    }
    /*компонент - Услуги*/
    #Services{
        /*бутстрап сетка*/
        .row{
            flex-direction: column-reverse;
        }
        /*кнопки*/
        button{
            width: 100%;
            margin-bottom: 5%;
        }
        /*бутстрап сетка*/
        .col-5{
            width: 100%;
        }
        /*svg*/
        svg{
            width: 50%;
            margin-left: 25%;
            margin-top: 0;
        }
    }
    /*компонент - Контакты*/
    #Contacts{
        /*бутстрап сетка*/
        .row{
            flex-direction: column;
            /*бутстрап сетка*/
            .row{
                flex-direction: row;
                /*бутстрап сетка*/
                .col{
                    margin-left: -12%;
                }
            }
        }
        /*блоки под информацию о контактах*/
        .contacts{
            margin: 0 0 2%;
            /*svg*/
            .row svg{
                margin-top: 0;
                width: 50%;
            }
        }
    }
}
@media screen and (min-width: 992px) and (max-width: 1200px){
    /*компоненты - Главная*/
    #Home{
        padding: 30px 0 60px 0;
    }
    /*компоненты - Главная, Направления, Преимущества, Лицензии, Сотрудники, Услуги, Контакты*/
    #About, #Directions, #Advantages, #Licenses, #Employees, #Services, #Contacts{
        padding: 40px 30px 40px;
    }
    /*заголовки*/
    h1{
        margin-top: 3% !important;
        font-size: 3.5rem !important;
        line-height: 4.5rem !important;
        margin-bottom: 0 !important;
    }
    h2{
        font-size: 2rem !important;
    }
    /*параграф*/
    p{
        margin-bottom: .5rem !important;
    }
    /*ссылки, жирный текст, список, параграф, пункты списка, текст*/
    a, b, u, p, li, .text, #Home p{
        font-size: 1.2rem;
        line-height: 1.4rem;
    }
    /*кнопки*/
    button, #Home button{
        font-size: 1.25rem !important;
    }
    /*список*/
    ul{
        margin-left: -2%;
        margin-bottom: 0 !important;
    }
    /*пункты списка*/
    li{
        margin-bottom: 1%;
    }
    /*ссылка в кнопке*/
    button a{
        font-size: 1.25rem !important;
    }
    /*компонент - Главная*/
    #Home{
        /*параграф*/
        p{
            width: 106%;
            margin: 0 0 4%;
        }
        /*svg*/
        svg{
            width: 94%;
            margin-left: 30px;
        }
        /*заголовки*/
        h2{
            font-size: 1.8rem !important;
        }
    }
    /*компонент - Преимущества (заголовок)*/
    #Advantages h2 {
        margin-top: 3% !important;
    }
    /*компонент - Лицензии*/
    #Licenses{
        /*svg*/
        svg{
            margin-top: 25%;
        }
        /*бутстрап сетка*/
        .col{
            padding-left: 0 !important;
            /*svg*/
            svg{
                margin: 0;
            }
        }
        /*отступы в таблице*/
        .table > :not(caption) > * > *{
           padding: 0.35rem 0.35rem !important;
        }
        /*первый столбец таблицы*/
        table tr td:first-child{
            width: 49%;
        }
    }
    /*компонент - Сотрудники (блок под svg)*/
    #Employees .svgEmployees{
        margin: 46px 15px 8px;
    }
    /*компонент - Контакты*/
    #Contacts{
        /*бутстрап сетка*/
        .contacts{
            margin: 10px;
            padding: 5px;
            /*svg*/
            .row svg{
                padding: 5px;
            }
        }
    }
}
@media screen and (min-width: 1200px) and (max-width: 1400px){
    /*компонент - Преимущества, Услуги(svg)*/
    #Advantages svg, #Services svg{
        width: 95%;
    }
    /*параграф*/
    p{
        margin-bottom: .5rem !important;
    }
    /*ссылки, жирный текст, список, параграф, пункты списка, текст*/
    a, b, u, p, li, .text, #Home p{
        font-size: 1.22rem;
        line-height: 1.4rem;
    }
    /*список*/
    ul{
        margin-left: -4%;
    }
    /*пункты списка*/
    li{
        margin-bottom: 2%;
    }
    /*ссылка в кнопке*/
    button a{
        font-size: 1.25rem !important;
    }
    /*заголовки*/
    h1{
        font-size: 4rem !important;
        line-height: 5rem !important;
        margin-bottom: 0 !important;
    }
    h2{
        font-size: 2.5rem !important;
    }
    /*кнопки*/
    button, #Home button{
        font-size: 1.25rem !important;
    }
    /*компонент - Главная*/
    #Home{
        /*svg*/
        svg{
            width: 94%;
            margin-left: 50px;
        }
        /*заголовки*/
        h2{
            font-size: 2rem !important;
        }
    }
    /*компонент - Лицензии (первый столбец таблицы)*/
    #Licenses table tr td:first-child{
        width: 55%;
    }
    /*компонент - Контакты (svg)*/
    #Contacts .contacts .row svg {
        padding: 5px;
    }
}
</style>
