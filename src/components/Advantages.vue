<template>
    <div id="Advantages">
        <b-container>
            <b-row>
                <b-col>
                    <h2>Почему выбирают нас</h2>
                    <ul v-for="list in List" class="ul">
                        <li class="text">{{list.text}}</li>
                    </ul>
                </b-col>
                <b-col>
                    <component :is="svg"/>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import AdvantagesSvg from "./svg/AdvantagesSvg";
    export default {
        name: "Advantages",
        data(){
            return{
                svg:AdvantagesSvg,
                List:[
                    {text:"Безупречная репутация",},
                    {text:"Личная сдача результата работы контролирующим органам",},
                    {text:"Лучший технадзор на рынке",},
                ],
            }
        }
    }
</script>

<style scoped lang="scss">
    #Advantages{
        padding: 4% 0 4%;
        .ul {
            padding:0;
            list-style: none;
        }
        .ul li:before {
            padding-right:10px;
            font-size: 2rem;
            font-weight: bold;
            color: #77AEDB;
            content: "\2606";
            transition-duration: 0.5s;
        }
        .ul li:hover:before {
            color: #337AB7;
            content: "\2605";
        }
        .col .flex-container > ul{
            width: 46%;
            margin: 1% 1.5% 1%;
        }
        .flex-container > ul {
            width: 22%;
            margin: 0 1% 6%;
        }
        .text{
            font-size: 1.45rem;
            line-height: 2rem;
        }
        svg{
            width: 100%;
            margin-bottom: 3%;
        }
    }
</style>
