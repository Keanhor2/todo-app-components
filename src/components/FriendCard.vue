<template>
    <div class="card" v-for="friend in friends" :key="friend">
        <div class="card-name">
            <h3>{{friend.firstName}} {{friend.lastName}}</h3>
        </div>
        <div class="card-comment">
            <p>{{friend.comment}}</p>
        </div>
    </div>
</template>

<script>
export default {
    props:["friends"]
}
</script>

<style>
    .card{
        margin:auto;
        width: 70%;
        margin-top:20px;
        padding: 20px;
        border-radius: 10px;
        box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px, rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
    }

</style>