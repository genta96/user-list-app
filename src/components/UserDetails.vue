<template>
    <div class="user-details">
        <router-link to="/"><h1>&larr;</h1></router-link>
        <img :src="user.picture.large" />
        <div class="info-div">
            <p><b>Name: </b>{{ user.name.title + " " + user.name.first + " " + user.name.last }}</p>
            <p><b>Date of Birth:</b> {{ user.dob.date }}</p>
            <p><b>Place of residence:</b> {{ user.location.city+", "+ user.location.state + ", "+ user.location.country }}</p>
            <p><b>E-mail:</b> {{ user.email }}</p>
            <p><b>Phone Number:</b> {{ user.phone}}</p>   
        </div>
    </div>
</template>

<script>
export default {
    name: "",
    data()  {
        return {
            user: JSON.parse(localStorage.getItem('userDetails'))
        }
    }
}
</script>

<style>
.user-details { margin-top: 60px; padding: 15px 10px; }
.user-details h1{font-weight: bold; margin-top: 0px;}
.user-details a {text-decoration: none; color: black; font-weight: bolder;}
.info-div {background-color: #FEFEFE; padding: 10px; box-shadow: 2px 1px 6px 1px #999;}
.info-div p {font-size: 25px; margin:5px 0px; }
</style>
