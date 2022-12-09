<template>
    <div id="About">
        <b-container>
            <b-row>
                <b-col cols="5">
                    <component :is="svg"/>
                </b-col>
                <b-col>
                    <h2>О нас</h2>
                    <p><b>ОАО "Группа компаний МАГ"</b> занимается строительно-монтажными и пуско-наладочными работами систем.</p>
                    <p><u>Наша компания состоит из:</u></p>
                    <ul>
                        <li><b>ООО "МРС"</b> - оператор связи и проектирование;</li>
                        <li><b>ООО "Аваконт"</b> - строительно-монтажные работы;</li>
                        <li><b>ООО "Гостехносервис"</b> - локальные и международные поставки.</li>
                    </ul>
                </b-col>
            </b-row>
            <p style="text-align: center"><u>Основные направления компании:</u></p>
            <div class="flex-container">
                <ul v-for="list in FirstList" class="ul">
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
        padding: 4% 3% 4%;
        h2{
            margin-top: 8%;
        }
        .ul {
            padding:0;
            //list-style: none;
            margin-bottom: .5rem !important;
            font-size: 1.2rem;
        }
        .col{
            ul {
                list-style: none !important;
            }
            li:before {
                padding-right:10px;
                margin-left: -3%;
                font-size: 2rem;
                color: #77AEDB;
                content: "\2727";
            }
            li:hover:before {
                color: #337AB7;
                content: "\2726";
            }
        }

        .flex-container > ul {
            width: 32%;
            list-style: none;
            padding: 1%;
            margin: .5%;
            box-shadow: 0 3px 6px -2px rgb(0 0 0 / 10%);
            border: 2px solid #b7dfe9;
            border-radius: 12px;
        }
        svg{
            width: 100%;
            margin-bottom: 3%;
        }
    }
</style>
