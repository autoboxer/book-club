<template>
    <TopNav @toggle-drawer="toggleDrawer" />
    <SideNav :is-open="isDrawerOpen" />
</template>

<script setup>
import { ref } from "vue";

const isDrawerOpen = ref(false);

const toggleDrawer = () => {
    isDrawerOpen.value = !isDrawerOpen.value;
};
</script>
