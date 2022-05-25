<template>
    <header>
        <h1>{{title}}</h1>
        <ButtonComp @toggle-add-task="$emit('toggle-add-task')" :text="showAddTask ? 'Close' : 'Add Task'" :color="showAddTask ? 'red': 'green'  "/>
    </header>
</template>

<script>
import ButtonComp from "./Button.vue";
    export default {
    name: "HeaderComp",
    props: {
        title: {
            type: String,
            default: "Title Here"
        },
        showAddTask: Boolean
    },
    components: { ButtonComp }
}
</script>

<style scoped>
header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}

</style>