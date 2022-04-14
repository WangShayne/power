<template>
    <ul  class="grid grid-flow-row grid-cols-3 grid-rows-3 gap-4 p-2">
        <li v-for="item in list" :key="item.id">
            <figure class="md:flex bg-gray-100 rounded-xl p-8 md:p-0">
                <img class="w-32 h-32 md:w-48 md:h-auto md:rounded-none rounded-full mx-auto" :src="item.avatar" alt="" width="384" height="512">
                <div class="pt-6 md:p-8 text-center md:text-left space-y-4">
                    <blockquote>
                    <p class="text-lg font-semibold">
                       {{item.description}}
                    </p>
                    </blockquote>
                    <figcaption class="font-medium">
                    <div class="text-cyan-600">
                        {{item.title}}
                    </div>
                    <div class="text-gray-500">
                        <a href="#">进入专栏</a>
                    </div>
                    </figcaption>
                </div>
            </figure>
        </li>
        
    </ul>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'
export interface ColumnListProps{
    id: number;
    title: string;
    avatar: string;
    description: string;
}

export default defineComponent({
    name: 'ColumnList',
    props: {
        list: {
            type: Array as PropType<ColumnListProps[]>,
            requird: true
        }
    },
    setup(props) {
        return {
            ...props
        }
    },
})
</script>
