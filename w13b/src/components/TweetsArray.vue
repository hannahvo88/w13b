<template>
    <div id="tweets" v-bind:style='{"display" : (isActive? "grid" : "block" )}'>
        <Tweet v-for="tweet in TweetsArray"
        :key="tweet.id"
        :id="tweet.id"
        :content="tweet.content"
        :author ="tweet.author"
        :date ="tweet.date"
        />
    </div>
</template>

<script>

import Tweet from './Tweet.vue'
    export default {
        name : "TweetsArray",
        props: {
            TweetsArray : Array,
        },
        components : {
            Tweet,
        },
      data() {
            return {
                isActive: true
            };
        },
        methods: {
            changeList: function(){
                this.isActive = !this.isActive;
            }
        },
        mounted : function () {
            this.$root.$on('changeList', this.changeList)

        }
    }
</script>

<style scoped>
body{
        margin: 0;
        font-family: 'TimeRoman';
        box-sizing: border-box;
        padding: 0 20px 0 20px;

}

#tweets{

    display:grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-column-gap:20px;
    justify-items: center;
    text-align: center;
    justify-content: center;
}

#tweet-item{
    width: 100%;
    max-width: 400px;
    margin: 40px auto;
    padding: 0 20px;
    box-sizing: border-box;
    border: solid 1px;

}

h2, p{
    text-align: center;
}

#toggle-button{
  margin-top:20px;
  display: flex;
  align-items: center;
  justify-content: center;
  }

button{
  text-align: center;
  padding: 5px 10px;
  background-color: blue;
  color: white;
  font-size: 1.5em;
}
</style>