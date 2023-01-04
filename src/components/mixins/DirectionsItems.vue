<template>
    <div class="wrapper">
        <div>
            <ul>
                <li v-for="item in items">{{item.text}}</li>
            </ul>
        </div>
    </div>
</template>

<script>
    export default {
        name: "DirectionsItems",
        props:{
            items: Array,
        }
    }
</script>

<style scoped>

</style>