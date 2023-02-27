<script lang="ts">
import {defineComponent} from 'vue'
export default defineComponent({
    data() {
        return{
            title: "Snackr Trackr"
        }
    }
})
</script>

<template>
    <v-layout>

        <v-toolbar
        dark
        >
            <v-app-bar-nav-icon></v-app-bar-nav-icon>
            <v-app-bar-title>{{title}} <v-icon icon="mdi-noodles"></v-icon> </v-app-bar-title>
        </v-toolbar>
    </v-layout>
</template>

<style scoped>
</style>