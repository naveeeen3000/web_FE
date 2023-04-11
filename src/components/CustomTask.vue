<template>
    <div class="container">
        <h2>Data Verification Custom Task</h2>    
        <form method="POST" action="results">
            <textarea v-model="authKey" placeholder="enter the auth key"  ></textarea>
            <textarea v-model="itemIds" placeholder="enter the item ids line by line"></textarea>
            <input type="submit" value="Done">
        </form>
    </div>
</template>



<script>
export default{
    data(){
        return {
            authKey: null,
            itemIds: null,
        }
    }
}
</script>

<style>
.container{
    text-align: center;
    color: black;
}
form{
    display: flex;
    flex-direction: column;
}
textarea{
    margin: 1vh;
    height: 300px;
}
input[type='submit']{
    font-weight: bold;
    font-size: large;
    margin: auto;
    border: 2px solid var(--blue);
}
</style>