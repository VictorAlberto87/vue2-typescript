<template>
    <div>
        <todo-list />
    </div>
</template>

<script lang="ts">
    import { Component, Vue } from "vue-property-decorator";
    import TodoList from "@/components/TodoList.vue";
    @Component ({
        components: {
            TodoList
        }
    })
    export default class TodoApp extends Vue {

    }

</script>

<style scoped>

</style>