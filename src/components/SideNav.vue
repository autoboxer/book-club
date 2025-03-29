<template>
    <v-navigation-drawer v-model="props.isOpen" temporary class="text-left">
        <v-list-item title="Selected Club" />
        <v-divider></v-divider>
        <v-list-item
            prepend-icon="mdi-book-open-blank-variant"
            link
            title="Book"
        />
        <v-list-item
            prepend-icon="mdi-calendar-multiselect"
            link
            title="Schedule"
        />
        <v-list-item prepend-icon="mdi-account-group" link title="People" />
        <v-list-item prepend-icon="mdi-forum" link title="Chat" />
        <v-list-item prepend-icon="mdi-message-video" link title="Meet" />
        <v-list-item prepend-icon="mdi-cog" link title="Settings" />
    </v-navigation-drawer>
</template>

<script setup>
const props = defineProps(["isOpen"]);
</script>
