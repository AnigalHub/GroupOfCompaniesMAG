<template>
    <div id="Advantages">
        <b-container>
            <b-row>
                <b-col>
                    <h2>Почему выбирают нас</h2>
                    <ul class="ul">
                        <li v-for="list in List" class="text">{{list.text}}</li>
                    </ul>
                    <b-button><a>Посмотреть лицензию</a></b-button>
                </b-col>
                <b-col cols="6">
                    <component :is="svg"/>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import HomeSvg from "./svg/HomeSvg";
    export default {
        name: "Advantages",
        data(){
            return{
                svg:HomeSvg,
                List:[
                    {text:"Безупречная репутация",},
                    {text:"Лучший технадзор на рынке",},
                    {text:"Выполнение всех работ точно в срок",},
                    {text:"Личная сдача результата работы контролирующим органам",},
                ],
            }
        }
    }
</script>

<style scoped lang="scss">
    #Advantages{
        .ul {
            padding:0;
            list-style: none;
        }
        .ul li{
           //font-weight: 600;
            padding-top: 1.5%;
            padding-bottom: 1.5%;
            padding-left: 2%;
        }
        .ul li:before {
            padding-right:10px;
            font-size: 2rem;
            font-weight: bold;
            color: #77AEDB;
            content: "\1F5F8";
            transition-duration: 0.5s;
        }
        .ul li:hover:before {
            color: #337AB7;
            content: "\2713";
        }
        svg{
            width: 100%;
            margin-top: -5%;
            margin-bottom: 10%;
        }
        .col-1 svg{
            width: 2.8rem;
            margin-top: 45%;
            margin-right: 15%;
        }
        button{
            width: 60%;
            margin: 1% 1.5%;
            padding: 1.5%;
            font-size: 1.5rem;
            border-radius: 30px;
            text-shadow: 1px 1px 0.2px rgb(0 0 0 / 43%);
            border: none;
            background: linear-gradient(to left, #b7dfe9,#adc7e2, #a0a6d8);
            a{
                color:white;
                text-decoration: none;
            }
        }
    }
</style>
