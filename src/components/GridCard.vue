<template>
    <div>
        <img :src="immagine" alt="testo">
        <h1>{{testo}}</h1>
    </div>
</template>

<script>
export default {
    name:'GridCard',
    data(){
        return{

        }
    },
    props:['immagine', 'testo']
}
</script>

<style lang="sass" scoped>

</style>