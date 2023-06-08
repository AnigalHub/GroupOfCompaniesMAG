<template>
    <div id="Contacts">
        <b-container>
            <h2>Свяжитесь с нами!</h2>
            <p>Мы проконсультируем вас по нашим услугам, подберем мастеров, согласуем удобное для вас
                время для проведения работ, и ответим на любой ваш вопрос.
            </p>
            <b-row class="text" >
                <b-col v-for="contact in Contacts" class="contacts">
                    <b-row>
                        <b-col cols="3">
                            <component :is="contact.svg"/>
                        </b-col>
                        <b-col>
                            <b>{{contact.name}}</b>
                            {{contact.description}}
                        </b-col>
                    </b-row>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import CallSvg from "./newSvg/Contacts/CallSvg";
    import MailSvg from "./newSvg/Contacts/MailSvg";
    import LocationSvg from "./newSvg/Contacts/LocationSvg";
    import information from '../../public/documents/information.json';
    export default {
        name: "Contacts",
        data() {
            return {
                Contacts: [
                    {
                        name:'Телефон',
                        description:information.phone,
                        svg:CallSvg,
                        href:'tel:' + information.phone,
                        target:'_self',
                    },
                    {
                        name:'Почта',
                        description:information.mail,
                        svg:MailSvg,
                        href:'mailto:' + information.mail,
                        target:'_self',
                    },
                    {
                        name:'Адрес',
                        description:information.address,
                        svg:LocationSvg,
                    },
                ],
            }
        }
    }
</script>

<style scoped lang="scss">

</style>