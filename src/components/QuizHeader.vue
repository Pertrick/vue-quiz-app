<script setup>
const {
    questionStatus,
    barPercentage
} = defineProps([
    'questionStatus',
    'barPercentage'
    ])
</script>

<template>
    <header>
      <h4>Question {{questionStatus}}</h4>
      <div class="bar">
        <div class="completion" :style="{width:barPercentage}"></div>
      </div>
    </header>
</template>

<style scoped>

header {
  margin-bottom: 10px;
  margin-top: 30px;
}

header h4{
  font-size: 20px;
}

.bar{
  width:300px;
  height:50px;
  border: 3px solid bisque;
}

.completion{
  height:100%;
  width:0%;
  background: bisque;
}

</style>