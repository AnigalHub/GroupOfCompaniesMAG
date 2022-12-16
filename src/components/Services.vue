<template>
    <div id="Services">
        <b-container>
            <b-row>
                <b-col>
                    <h2>Мы предоставляем услуги:</h2>
                    <ul v-for="list in List" class="ul">
                        <li class="text">{{list.text}}</li>
                    </ul>
                    <b-button><a>Узнать цены на виды работ</a></b-button>
                </b-col>
                <b-col cols="5">
                    <component :is="svg"/>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    // import AdvantagesSvg from "./svg/AdvantagesSvg";
    import ServicesSvg from "./svg/ServicesSvg"
    export default {
        name: "Services",
        data(){
            return{
                svg:ServicesSvg,
                List:[
                    {text:"Проектирование",},
                    {text:"Согласование проекта",},
                    {text:"Выполнение строительно-монтажных работ",},
                    {text:"Сдача объекта технадзору заказчика и контролирующим органам",},
                    {text:"Подготовка исполнительной документации",},
                ],
            }
        }
    }
</script>

<style scoped lang="scss">
    #Services{
        ul li{
            padding: .5%;
        }
        svg{
            width: 100%;
        }
        button{
            width: 65%;
            margin: 1% 1.5%;
            padding: 2%;
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
