<template>
<div>
    <h1>This is the Jokes page</h1>
    <div v-for="joke in jokes" :key="joke.id">
        {{joke.joke}}

    </div>
</div>

</template>

<script>
export default {
    name:"Jokes",
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