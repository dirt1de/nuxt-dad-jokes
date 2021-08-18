<template>
<div>
    <h1>This is the Jokes page</h1>
    <Joke v-for="joke in jokes" :key="joke.id" :joke="joke.joke"></Joke>
</div>

</template>

<script>
import Joke from "../components/Joke.vue"
export default {
    name:"Jokes",
    components:{
        Joke
    },
    data(){
        return{
            jokes:[]
        }
    },
    created(){
        const config={
            headers:{
                Accept:"application/json"
            }
            
        }
        fetch("https://icanhazdadjoke.com/search", config)
        .then(res=>res.json())
        .then(data=>{
            this.jokes=data.results
        })
    
    }

}
</script>

<style>

</style>