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
            }
        }
    }
</script>

<style scoped lang="scss">
    #About{
        h2{
            margin-top: 5%;
        }
        ul {
            padding: 0 3% 2% 3%;
            margin-bottom: 1.5% !important;
            font-size: 1.2rem;
            list-style: none !important;
        }
        li:before {
            padding-right: 10px;
            margin-left: -3%;
            font-size: 1.5rem;
            color: #77AEDB;
            content: "\25cb";
        }
        li:hover:before {
            color: #337AB7;
            font-size: 1.55rem;
            content: "\2022";
        }
        svg{
            width: 100%;
            margin-bottom: 3%;
        }
    }
</style>
