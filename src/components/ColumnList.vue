<template>
  <ul class="grid grid-flow-row grid-cols-3 grid-rows-3 gap-4 p-4">
    <li v-for="item in list" :key="item.id">
        <div class="p-6 flex bg-gray-100 rounded-xl mx-auto items-center">
          <div class="flex-shrink-0">
            <img class="w-40 h-48" :src="item.avatar" alt="avatar">
          </div>
          <div class="p-12 flex flex-col items-center">
            <h1 class="text-xl font-medium text-black text-center truncate">{{item.title}}</h1>
            <p class="h-24 text-gray-500 text-left overflow-ellipsis overflow-hidden">{{item.description}}</p>
            <button class="mt-6 py-2 px-4 w-32 font-semibold rounded-lg shadow-md text-white bg-green-500 hover:bg-green-700">进入专栏</button>
          </div>
        </div>
    </li>
  </ul>
</template>

<script lang="ts">
import { defineComponent, PropType } from "vue";
export interface ColumnListProps {
  id: number;
  title: string;
  avatar: string;
  description: string;
}

export default defineComponent({
  name: "ColumnList",
  props: {
    list: {
      type: Array as PropType<ColumnListProps[]>,
      requird: true,
    },
  },
  setup(props) {
    return {
    };
  },
});
</script>
