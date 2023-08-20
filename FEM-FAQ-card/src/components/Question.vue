<template>
    <div>
        <p>{{ question }}</p>
        <img 
        v-on:click="changeDisplay"
        src="../assets/images/icon-arrow-down.svg"/>
    </div>
    <p v-show="displayAnswer">{{ answer }}</p>
</template>

<script>
    export default {
        data() {
            return { 
                displayAnswer: false,
            }
        },
        methods: {
            changeDisplay() {
                this.displayAnswer = !this.displayAnswer;
            }
        },
        props: {
            question: {
                type: String, 
                default: 'This is a question'
            },
            answer: {
                type: String,
                default: 'This is an answer.'
            }
        }
    }
</script>

<style>

</style>