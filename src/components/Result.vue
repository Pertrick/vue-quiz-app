<script setup>
import { RouterLink } from "vue-router";
const  {numberOfCorrectAnswers, quizQuestionLength} = 
defineProps(["numberOfCorrectAnswers","quizQuestionLength"])

</script>

<template>
    <div class="results">
        <p>Your Results...</p>
        <h1>
            {{numberOfCorrectAnswers}} / {{ quizQuestionLength }}
        </h1>
        <RouterLink to="/">
            <button type="button">Go Back</button>
        </RouterLink>
    </div>
</template>

<style scoped>
    .results{
        text-align: center;
        padding: 100px 0;
    }

    p{
        font-size:25px;
    }

    h1{
        font-size: 80px;
    }

    button{
        padding: 10px;
        font-size:20px;
        border-radius: 5px;
        cursor: pointer;
        border:none;
    }


</style>