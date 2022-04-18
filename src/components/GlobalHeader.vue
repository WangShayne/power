<template>
    <nav class="w-full flex justify-between p-2">
        <div>
            <h1 class="text-green-700">Logo</h1>
        </div>
        <div v-if="!user.isLogin">
            <button class="inline mt-6 py-2 px-4 w-32 font-semibold rounded-lg shadow-md text-white bg-green-500 hover:bg-green-700">登录</button>
            <button class="inline mt-6 py-2 px-4 w-32 font-semibold rounded-lg shadow-md text-white bg-green-500 hover:bg-green-700">注册</button>
        </div>
        <div v-else>
            hello,{{user.userName}}
            <ul>
                <li>
                    个人中心
                </li>
            </ul>
        </div>
        
    </nav>
</template>

<script setup lang="ts">import { PropType } from 'vue';

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