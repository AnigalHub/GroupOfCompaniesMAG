<template>
    <div id="About">
        <b-container>
            <b-row>
                <b-col cols="5">
                    <component :is="svg"/>
                </b-col>
                <b-col>
                    <h2>
                        О нас
                    </h2>
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
                    { text:"Контроля и управления доступом (СКУД)",},
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
        }
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
            margin: 0 1% 2%;
        }
        p{
            margin: 2% 0;
        }
        p,li,.text{
            font-size: 1.4rem;
            line-height: 2rem;
        }
        svg{
            width: 105%;
            margin-bottom: 3%;
        }
    }
</style>
