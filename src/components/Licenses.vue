<template>
    <div id="Licenses">
        <b-container>
            <h2>Лицензии на предоставляемые услуги</h2>
            <b-row>
                <b-col cols="5">
                    <component :is="svg"/>
                </b-col>
                <b-col>
                    <table class="table">
                        <tbody>
                            <tr v-for="(license, index) in Licenses" :key="index" class="text">
                                <td> {{license.text}}</td>
                                <td>
                                    <a @click="showModal(license)"><span> Просмотр</span><component :is="viewSvg"/></a>
                                </td>
                                <td>
                                    <a :href="license.href" download><span>Скачать</span><component :is="downloadSvg"/></a>
                                </td>
                            </tr>
                        </tbody>
                    </table>
                </b-col>
            </b-row>
            <b-modal ref="my-modal" id="img" size="lg" centered>
                <iframe :src="selectedLicense.href" width="100%" height="100%"/>
            </b-modal>
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
                selectedLicense:{
                    href:''
                },
                Licenses:[
                    {href:"./documents/Телематические услуги связи.pdf", text:"Телематические услуги связи",},
                    {href:"./documents/Услуги связи для целей проводного радиовещания.pdf", text:"Услуги связи для целей проводного радиовещания",},
                    {href:"./documents/Услуги связи по передаче данных, за исключением услуг связи по передаче данных для целей передачи голосовой информации.pdf", text:"Услуги связи по передаче данных, за исключением услуг связи по передаче данных для целей передачи голосовой информации",},
                    {href:"./documents/Услуги связи по предоставлению каналов связи.pdf", text:'Услуги связи по предоставлению каналов связи'},
                    {href:"./documents/Деятельность по монтажу, техническому обслуживанию и ремонту средств обеспечения пожарной безопасности зданий и сооружений.pdf", text:"Деятельность по монтажу, техническому обслуживанию и ремонту средств обеспечения пожарной безопасности зданий и сооружений",},
                ],
                viewSvg:ViewSvg,
                downloadSvg: DownloadSvg
            }
        },
        methods: {
            showModal(license) {
                this.selectedLicense = license;
                this.$refs['my-modal'].show()
            },
        }
    }
</script>
<style scoped lang="scss">

</style>

