<template>
    <p>Reaction Time : {{ score }}ms</p>
    <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return{
            rank: null
        }
    },
    mounted() {
        if(this.score < 250){
            this.rank = 'Ninja Fingers'
        } else if (this.score < 400){
            this.rank = 'Rapid Reflexes'
        } else if (this.score < 600){
            this.rank = 'Respectable Speed'
        } else if (this.score < 800){
            this.rank = 'You can do better'
        } else {
            this.rank = 'Snail pace...'
        }
    }
}
</script>

<style>
    .rank{
       font-size: 1.4em;
       color: #0faf87;
       font-weight: bold; 
    }
</style>