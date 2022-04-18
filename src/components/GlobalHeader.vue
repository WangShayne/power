<template>
    <nav class="w-full flex justify-between p-2 bg-green-500">
        <div>
            <h1 class="text-2xl font-bold text-white">Logo</h1>
        </div>
        <div v-if="!user.isLogin">
            <button class="inline py-2 px-4 w-24 font-semibold rounded-lg shadow-md text-white bg-green-700 hover:bg-white hover:text-black">登录</button>
            <button class="inline py-2 px-4 w-24  ml-2 font-semibold rounded-lg shadow-md text-white bg-green-700 hover:bg-white hover:text-black">注册</button>
        </div>
        <div v-else>
            <DropDown :title="`Hello,${user.userName}`" />
        </div>
        
    </nav>
</template>

<script setup lang="ts">
import { PropType } from 'vue'
import DropDown from './DropDown.vue'
/**
 * user props
 * isLogin
 * username
 * id
 */
export interface UserProps{
    isLogin: boolean;
    userName?: string;
    id?: number;
}

defineProps({
    user:{
        type: Object as PropType<UserProps>,
        required: true
    }
})


</script>

<style>


</style>