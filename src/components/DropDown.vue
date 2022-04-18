<template>
    <div class="relative w-32">
        <a href="#" @click.prevent="toggleOpen">{{title}}</a>
        <ul :class="isOpen ? 'block' : 'hidden'" class="absolute bg-white w-full">
            <li class="py-2 cursor-pointer hover:text-green-700">
                个人中心
            </li>
            <li class="py-2 cursor-pointer hover:text-green-700">
                退出登录
            </li>
        </ul>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

defineProps({
    title: {
        type: String,
        required: true
    }
})

const isOpen = ref(false)
const toggleOpen = () => {
    isOpen.value = !isOpen.value
}

</script>