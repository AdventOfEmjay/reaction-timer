<template>
    <p>Reaction Time - {{ score }} ms</p>
    <p class="rank">{{ rank }}</p>
</template>
<script>
export default {
    props: ['score'],
    data(){
        return{
            rank: null
        }
    },
    mounted(){
        if(this.score < 300){
            this.rank = 'Ninja Fingers Mate!!!'
        } else if (this.score < 350){
            this.rank = 'Rapid Reflexes Mate!!'
        } else if (this.score < 400){
            this.rank = 'Cmon mate are you even trying???'
        } else {
            this.rank = 'Buzz off slow poke'
        }
    }
}
</script>
<style>
.rank{
    color: darkcyan;
    font-weight: bold;
    font-size: 1.4rem
}
</style>