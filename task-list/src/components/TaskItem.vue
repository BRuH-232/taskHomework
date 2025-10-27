<template>
  <div class="task-card">
    <header>
      <div class="task-name"><b>{{ props.task.title }}</b></div>
    </header>

    <main>
      <div class="task-description">{{ props.task.text }}</div>
    </main>

  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  task: { title: string; text: string };
}>();


</script>

<style>
.task-card {
  display: flex;
  gap: 20px;
  flex-direction: row;
  border: 3px solid #ccc;
  padding: 12px;
  border-radius: 30px;
  box-shadow: 2px 2px 9px 1px #727;
}
.task-name{
  font-size: 28px;
  padding: 20px;
}
.task-description{
  width: 300px;
  margin: 5px;
  padding: 15px; 
  border: 3px solid #ccc;
  border-radius: 15px;
  box-shadow: 2px 2px 9px 1px #727;
}
</style>