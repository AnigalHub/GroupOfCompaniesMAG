<template>
    <b-navbar id="Nav" class="navbar-expand-xl sticky-top" toggleable>
        <b-container>
            <b-navbar-brand href="#Home" @click="scrollToId">
                <component :is="svg"/> <span class="description_name">ГК «МАГ»</span>
            </b-navbar-brand>
            <b-navbar-toggle target="navbar-toggle-collapse">
                <template v-slot:default="{ expanded }">
                    <b-icon v-if="expanded" icon="chevron-bar-up"></b-icon>
                    <b-icon v-else icon="chevron-bar-down"></b-icon>
                </template>
            </b-navbar-toggle>
            <b-collapse id="navbar-toggle-collapse" class="justify-content-end" is-nav v-model="isExpanded">
                <b-navbar-nav>
                    <b-nav-item @click="scrollToId" href="#About">О нас</b-nav-item>
                    <b-nav-item @click="scrollToId" href="#Directions">Направления</b-nav-item>
                    <b-nav-item @click="scrollToId" href="#Advantages">Преимущества</b-nav-item>
                    <b-nav-item @click="scrollToId" href="#Licenses">Лицензии</b-nav-item>
                    <b-nav-item @click="scrollToId" href="#Employees">Коллектив</b-nav-item>
                    <b-nav-item @click="scrollToId" href="#Services">Услуги</b-nav-item>
                    <b-nav-item @click="scrollToId" href="#Contacts">Контакты</b-nav-item>
                </b-navbar-nav>
            </b-collapse>
        </b-container>
    </b-navbar>
</template>

<script>

    import Favicon from "./newSvg/Favicon";

    export default {
        name: "navbar",

        data(){
            return{
                svg:Favicon,
                isExpanded: false,
            }
        },
        methods:{
            scrollToTop(){
                window.scrollTo({top: 0, left: 0, behavior: 'smooth' });
            },
            scrollToId(event){
                let offsetY = 20;
                if(this.isExpanded){
                    let nav = document.getElementById(("Nav"));
                    let bounds =  nav.getBoundingClientRect();
                    offsetY = bounds.height;
                }
                let element = document.getElementById(event.target.hash.replace("#", ""));
                window.scrollTo({top: element.offsetTop - offsetY, left: 0, behavior: 'smooth'});
                event.preventDefault();
            }
        }
    }
</script>

<style scoped lang="scss">
    /*текст при раскрытом меню в мобильном варианте*/
    .navbar-light .navbar-toggler {
        color: #3798c5;
    }
    .navbar-nav{
        margin-bottom: 0 !important;
    }
    /*блок под логотип(картинка, название компании, что за компания(производственная))*/
    .navbar-brand{
        padding-top: 0.2rem !important;
        padding-bottom: 0.2rem !important;
    }
    /*меню на всех экранах (которое будет и складываться на маленьких экранах и раскрываться на больших)*/
    .navbar{
        background:#f2f4f6;
        background-size:cover;
        border-bottom: 5px #8792a5 !important;
        //box-shadow: 7px 7px 7px -7px rgb(34 60 80 / 90%);
        padding: 5px 0;
        li {margin-bottom: 0 !important;}
        svg{
            width: 40px;
        }
    }
    /*все кнопки в меню*/
    .nav-link{
        color: rgb(112 112 112) !important;
        padding-right: 1rem !important;
        padding-left: 1rem !important;
        font-family: 'Tinos', serif;
        font-size: 1.35rem ;
        &:hover{
            color: black !important;
        }
    }
    /*надпись "производственная компания" в логотипе*/
    .description_name{
        font-family: 'Roboto Condensed', sans-serif;
        color: #8792a5;
        padding-top: 30px;
        letter-spacing: 2px;
        font-weight: 600;
        //text-shadow: 0.025rem 0.025rem 0.025rem #8792a5;
    }
    /*АДАПТИВНОСТЬ*/
    @media screen and (max-width: 768px) {
        /*все кнопки в меню*/
        .nav-link {
            font-size: 1.15rem;
            padding: 0.35rem 1rem !important;
        }
    }
</style>