<template>
    <div id="Advantages">
        <b-container>
            <b-row>
                <b-col>
                    <h2>Почему выбирают нас</h2>
                    <ul class="ul">
                        <li v-for="list in List" class="text">{{list.text}}</li>
                    </ul>
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
        padding: 4% 3% 0;
        .ul {
            padding:0;
            list-style: none;
        }
        .ul li{
           font-weight: 600;
            padding-top: 2%;
            padding-bottom: 3%;
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
    }
</style>
