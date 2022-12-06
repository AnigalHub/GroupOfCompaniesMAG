<template>
    <div id="About">
        <b-container>
            <b-row>
                <b-col cols="6">
                    <component :is="svg"/>
                </b-col>
                <b-col>
                    <h2>О нас</h2>
                    <p>
                        <b>ОАО "Группа компаний МАГ"</b>- группа компаний, занимающаяся строительно-монтажными и пуско-наладочными работами систем:
                    </p>
                    <div class="flex-container">
                        <ul v-for="list in FirstList" class="ul">
                            <li class="text">{{list.text}}</li>
                        </ul>
                    </div>
                </b-col>
            </b-row>
            <div class="flex-container">
                <ul v-for="list in SecondList" class="ul">
                    <li class="text">{{list.text}}</li>
                </ul>
            </div>
        </b-container>
    </div>
</template>

<script>
    import AboutSvg from "./svg/AboutSvg";
    export default {
        name: 'About',
        data(){
            return{
                svg:AboutSvg,
                FirstList:[
                    {text:"Оповещения населения (ГОиЧС)",},
                    {text:"Дератизационные системы (ОЗДС) ",},
                    {text:"Пожарные сигнализации (СПС, АПС)",},
                    {text:"Контроля и управления доступом (СКУД)",},
                ],
                SecondList:[
                    {text:"Контроля учета электроэнергии (АСКУЭ)",},
                    {text:"Охранные комплексы и различный мониторинг",},
                    {text:"Проводного радиовещания (РСО, РАСЦО)",},
                    {text:"Оповещения и управления эвакуацией (СОУЭ)",},
                    {text:"Каналов связи (оптические, электрические, беспроводные)",},
                    {text:"Управления и диспетчеризация инженерных систем (АСУД)",},
                    {text:"Видеонаблюдения (СОТ, Безопасный регион, Безопасный город)",},
                    {text:"Электрические сети и установки (Бытовые и промышленные до 220КВ)",},
                ],
            }
        }
    }
</script>

<style scoped lang="scss">
    .flex-container{
        display: flex;
        flex-wrap: wrap;
    }
    #About{
        h2{
            margin-top: 5%;
            margin-left: -8%;
        }
        padding: 4% 3% 4%;
        .ul {
            padding:0;
            list-style: none;
            margin-bottom: .8rem !important;
            font-size: 1.2rem;
        }
        .ul li:before {
            padding-right:10px;
            font-size: 2rem;
            font-weight: bold;
            color: #77AEDB;
            content: "\2999";
            transition-duration: 0.5s;
        }
        .col .flex-container{
            margin-left: -6%;
        }
        .col .flex-container > ul{
            width: 100%;
            margin: 1% 1.5% 1%;
        }
        .flex-container > ul {
            width: 46%;
            margin: 0 1% 2%;
        }
        p{
            margin-top: 2%;
            margin-bottom: 2%;
            margin-left: -8%;
        }
        svg{
            width: 95%;
            margin-bottom: 3%;
        }
    }
</style>
