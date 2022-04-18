<template>
    <GlobalHeader :user="userData"/> 
    <ColumnList :list="testData"/> 
</template>

<script setup lang="ts">
import ColumnList, { ColumnListProps } from "./components/ColumnList.vue";
import GlobalHeader, { UserProps } from "./components/GlobalHeader.vue";
const userData: UserProps = {
  isLogin: true,
  userName: "Shayne"
}
const testData: ColumnListProps[] = [
  {
    id: 0,
    title: 'test1',
    description: 'this is a test description',
    avatar: 'https://avatars.githubusercontent.com/u/17644818?v=4'
  },
  {
    id: 2,
    title: 'test1',
    description: 'this is a test descriptionthis is a test descriptionthis is a test descriptionthis is a test descriptionnthis is a test descriptionnthis is a test description',
    avatar: 'https://avatars.githubusercontent.com/u/17644818?v=4'
  },
  {
    id: 3,
    title: 'test1',
    description: 'this is a test description',
    avatar: 'https://avatars.githubusercontent.com/u/17644818?v=4'
  },
  {
    id: 4,
    title: 'test1',
    description: 'this is a test description',
    avatar: 'https://avatars.githubusercontent.com/u/17644818?v=4'
  }
]
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
