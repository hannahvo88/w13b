<template>
  <div id="app" >
    <img alt="Vue logo" src="./assets/logo.png">
    <Button />
    <TweetsArray v-bind:TweetsArray="tweets" />
  </div>
</template>

<script>
import Button from './components/Button.vue'
import TweetsArray from './components/TweetsArray.vue'

export default {
  name: 'App',
  components: {
    Button,
    TweetsArray
  },
  data (){
    return{
      tweets :[
        {
            id: 1,
            content :"WhatsApp cofounder: It's time to delete Facebook",
            author :"John",
            date : "01-01-2018",
         
        },

        {   
          id : 2,
          content:"Shockingly awful work conditions",
            author:"Mark",
            date : "02-31-2021",
            
        },

        {
            id : 3,
            content :"No one is born hating another person because of the color of his skin or his background or his religion...",
            author :"Bilge",
            date : "08-08-2019",
            
        },

        {
            id :4,
            content :"Can't lose the 2020 election if there is no 2020.",
           author:"Peter",
            date: "01-07-2018",
            
        },
      ]
  }
}}
</script>

<style>

</style>
