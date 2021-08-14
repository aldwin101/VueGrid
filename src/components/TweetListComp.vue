<template>
    <div>
        <h1>{{tweetCreator}}</h1>
        <h3>{{tweetContent}}</h3>
        <p>{{tweetCreated}}</p>
    </div>
</template>

<script>
    export default {
        name : 'TweetListComp',
        props : {
            tweetContent : String,
            tweetCreator : String,
            tweetCreated : String
        }
}
</script>

<style scoped>
div {
    border-radius: 20px;
    margin: 20px;
    background-color: rgb(241, 232, 241);
}
h1 {
    color: black;
}
h1, h3, p {
    margin: 5px 25px;
}
</style>