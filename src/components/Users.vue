<template>
    <div class="container">
    <h2>Users</h2>
    <table class="table">
        <thead>
            <tr>
                <th>Id</th>
                <th>Name</th>
                <th>Username</th>
                <th>Email</th>
                <th>City</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="user in users" v-bind:key="user.id">
                <td>{{user.id}}</td>
                <td>{{user.name}}</td>
                <td>{{user.username}}</td>
                <td>{{user.email}}</td>
                <td>{{user.address.city}}</td>
            </tr>
        </tbody>

    </table>
    </div>
</template>

<script>
import axios from 'axios'
export default {
    name:'Users',

    data(){
        return {
            users:null,
        }
    },
    created : function(){
        axios.get('https://jsonplaceholder.typicode.com/users')
        .then((res)=>{
            this.users = res.data
            console.log(this.users)
        })
    }
}
</script>
<style scoped>
h3{
    margin-bottom: 5%;
}
</style>