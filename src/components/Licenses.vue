<template>
    <div id="Licenses">
        <b-container>
            <h2>Лицензии на предоставляемые услуги</h2>
            <b-row>
                <b-col cols="5">
                    <component :is="svg"/>
                </b-col>
                <b-col >
                    <table class="table">
                        <tbody>
                            <tr v-for="license in Licenses" class="text">
                                <td> {{license.text}}</td>
                                <td>
                                    <span> Просмотр</span><component :is="viewSvg"/>
                                </td>
                                <td>
                                    <span> Скачать</span><component :is="downloadSvg"/>
                                </td>
                            </tr>
                        </tbody>
                    </table>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import AdvantagesSvg from "./newSvg/Main/LicensesSvg";
    import ViewSvg from "@/components/newSvg/Licenses/ViewSvg";
    import DownloadSvg from "@/components/newSvg/Licenses/DownloadSvg";
    export default {
        name: "Licenses",
        data(){
            return{
                modalShow: false,
                svg:AdvantagesSvg,
                Licenses:[
                    {img_src:"./documents/license-1.png", text:"Телематические услуги связи",},
                    {img_src:"./documents/license-1.png", text:"Услуги связи для целей проводного радиовещания",},
                    {img_src:"./documents/license-1.png", text:"Услуги связи по передаче данных, за исключением услуг связи по передаче данных для целей передачи голосовой информации",},
                    {img_src:"./documents/license-1.png", text:'Услуги связи по предоставлению каналов связи'},
                    {img_src:"./documents/license-1.png", text:"Деятельность по монтажу, техническому обслуживанию и ремонту средств обеспечения пожарной безопасности зданий и сооружений",},
                ],
                viewSvg:ViewSvg,
                downloadSvg: DownloadSvg
            }
        },
    }
</script>
<style scoped lang="scss">

</style>

