<template>
<div>
    <form @submit.prevent="createPost">
        <label for="userId">Unser Id</label>
        <input id="userId" v-model="formData.userId"/><br>
        <label for="title">title</label>
        <input id="title" v-model="formData.title"/><br>
        <label for="body">body</label>
        <input id="body" v-model="formData.body"/>

        <button> create post</button>
    </form>
</div>
</template>

<script>
import axios from 'axios'
export default {
    name:'CreatePost',
    data(){
        return{
            formData:{
                userId:'',
                title:'',
                body:''
            }
        }
    },
    methods:{
        createPost(){
            axios.post('https://jsonplaceholder.typicode.com/posts',this.formData)
            .then((response)=>{
                console.log(response)
            }).then((error)=>{
                console.log(error)
            })
        }
    }
}
</script>

<style>
</style>