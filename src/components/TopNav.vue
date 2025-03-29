<template>
    <v-app-bar color="teal-darken-4" class="text-center">
        <template v-slot:image>
            <v-img
                gradient="to top right, rcburgba(19,84,122,.8), rgba(128,208,199,.8)"
            ></v-img>
        </template>

        <template v-slot:prepend>
            <v-app-bar-nav-icon @click="$emit('toggle-drawer')" />
        </template>

        <v-app-bar-title class="cursor-default">Book Club</v-app-bar-title>

        <v-btn icon v-if="loggedIn">
            <v-icon>mdi-account</v-icon>
        </v-btn>
        <span v-else class="pr-4 cursor-pointer">Login</span>

        <v-btn icon>
            <v-icon>mdi-book</v-icon>
        </v-btn>

        <v-btn icon>
            <v-icon>mdi-dots-vertical</v-icon>
        </v-btn>
    </v-app-bar>
</template>

<script setup>
import { ref } from "vue";

const loggedIn = ref(false);

const handleDrawerToggleClick = () => {
    emit("toggle-drawer");
};
</script>
