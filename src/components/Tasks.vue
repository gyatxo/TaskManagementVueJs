<template>
    <div v-for="task in tasks" :key="task.id">
        <TaskComp :task="task" @toggle-reminder="$emit('toggle-reminder',task.id)" @delete-task="$emit('delete-task',task.id)"/>
    </div>
</template>

<script>
import TaskComp from './Task.vue';
    export default {
    name: "TasksComp",
    props: {
        tasks: Array,
    },
    emits: ['delete-task','toggle-reminder'],
    components: { TaskComp }
}
</script>

<style>
</style>