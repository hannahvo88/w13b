<template>
    <div id="tweet-item">
        <h2>{{author}}</h2>
        <p>{{content}}</p>
        <p>{{date}}</p>
    </div>
</template>

<script>
    export default {
    name: 'Tweet',
    props :{
        id:{
            type:Number,
            required:true,
        },
        content:{
            type:String,
            required:true,
        },
        author:{
            type:String,
            required:true,
        },
        date:{
            type:String,
            required:true,
        }
    },    
        
};
</script>

<style scoped>

</style>