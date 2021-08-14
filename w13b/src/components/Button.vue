<template>
    <div id="toggle-button">
        <button @click="toggleTheList">Click Me</button>
    </div>
</template>

<script>
    export default {
        methods:{
            toggleTheList: function(){
                this.$root.$emit('changeList')
            }
        },
    }
</script>

<style scoped>

</style>