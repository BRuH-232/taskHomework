<template>
  <div>
    <h1 class="site-description">Список дел</h1>

    <div class="tasks">
      <TaskItem
        v-for="task in tasks" 
        :task="task"
      />
    </div>

  </div>
</template>


<script setup lang="ts">
//import { ref, computed } from "vue";
import TaskItem from "./components/TaskItem.vue";

const tasks = [
  { _id: "1", title: "Убока дома:", text: "Убрать квартиру: помыть полы, \
  протереть пыль, пропылесосить."},
  { _id: "2", title: "Покупка продуктов:", text: "Купить продукты: макароны, помидоры, \
  морковь, свинной фарш."},
  { _id: "3", title: "Готовка ужина:", text: "Приготовить макароны со свинным фаршом \
  под томатным соусом."},
  { _id: "4", title: "Подготовка ко сну:", text: "Выполнить стандартные ритуалы: \
  помыться, побриться, лечь под одеялко."},
];

</script>

<style>
.site-description{
  height: 70px;
  width: 350px;
  border-radius: 15px;
  box-shadow: 0px 7px 5px 0px #ccc;
  margin: 40px auto;
}
.tasks {
  display: flex;
  gap: 16px;
  flex-direction: column;
}
</style>