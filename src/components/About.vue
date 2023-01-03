<template>
    <div id="About">
        <b-container>
            <b-row>
                <b-col cols="4">
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

</style>
