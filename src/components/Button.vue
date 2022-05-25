<template>
    <button @click="onClick()" :style="{backgroundColor: color}" class="btn">
    {{text}}
    </button>
</template>

<script>

    export default {
        name: 'ButtonComp',
        props:{
            text: {
            type: String,
            default: 'Add'
            },
            color: {
            type: String,
            default: 'black'
            }
        },
        methods:{
            onClick(){
                this.$emit('toggle-add-task')
            }
        }
    }
</script>