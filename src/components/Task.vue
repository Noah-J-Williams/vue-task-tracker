<template>
    <div class="task">
        <h3>{{ task.text }}</h3>
        <i class="icon">[X]</i>
        <p>{{ task.day }}</p>
    </div>
</template>

<script>
    export default{
        name: "Task",
        props: {
            task: Object
        }
    }
</script>

<style scoped>

    .task {
        background: #f4f4f4;
        margin: 0.5rem;
        padding: 1rem 1.5rem;
        cursor: pointer;
    }

    .task.reminder {
        border-left: 5px solid green;
    }

    .task h3 {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
</style>