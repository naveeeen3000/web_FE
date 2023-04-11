<script setup>
import {RouterLink} from "vue-router";
</script>

<template>
    <div class="navbar">
        <div class="brand"></div>
        <div class="nav">
            <router-link class="link" to="leetcode"><div class="single-nav"><h2>Leet-code</h2></div></router-link>
            <router-link class='link' to="custom_task"><div class="single-nav"><h2>Custom Task</h2></div></router-link>
            
        </div>
    </div>
</template>


<style scoped>
    @import "../assets/main.css" ;
    @import "../assets/base.css" ;

    .link{
        text-decoration: none;
        color: var(--blue);
    }
    .navbar .nav{
        display:flex;
        justify-content: space-evenly;

    }

    .link{
        padding: 0 1rem 0 1rem;
        /* height: 5vh; */
        text-align: center;
    }
    .link:hover{
        transition: 0.35s;
        background-color: var(--blue);
        color: var(--color-background);
    }
</style>
