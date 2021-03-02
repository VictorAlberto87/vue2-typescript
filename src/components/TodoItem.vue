<template>
    <tr>
        <td class="px-4 py-3">{{ index + 1 }}</td>
        <td class="px-4 py-3">{{ todo }}</td>
        <td class="px-4 py-3">
            <button @click="$emit('removeTodo')" class="inline-flex items-center bg-red-400 text-white border-0 py-1 px-3 leading-3 focus:outline-none rounded text-sm mt-4 md:mt-0">
                Eliminar
            </button>
        </td>
    </tr>
</template>

<script lang="ts">
    import { Component, Prop, Vue } from "vue-property-decorator";
    @Component
    export default class TodoItem extends Vue {
        @Prop() todo!: string;
        @Prop() index!: number;
    }
</script>