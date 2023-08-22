<template>
    <div class="question">
        <p>{{ question }}</p>
        <img 
        v-on:click="changeDisplay"
        src="../assets/images/icon-arrow-down.svg"/>
    </div>
    <p v-show="displayAnswer">{{ answer }}</p>
    <hr>
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
    @import url('https://fonts.googleapis.com/css2?family=Kumbh+Sans:wght@400;700&display=swap');

    html {
        font-family: 'Kumbh Sans';
    }

    p {
        color: hsl(238, 29%, 16%);
    }

    .question {
        display: flex;
        margin: 10px 0px;
        font-weight: 700;
    }


</style>