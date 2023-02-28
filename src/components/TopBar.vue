<script lang="ts">
import {defineComponent} from 'vue'
export default defineComponent({
    data() {
        return{
            drawer: false,
            title: "Snackr Trackr",
            items: [
                {title: 'Login', path:'/'},
                {title: 'Snacks', path:'/snacks'}
            ],
        }
    }
})
</script>

<template>
    <v-layout>

        <v-toolbar
        dark
        >
            <!-- <v-app-bar-nav-icon></v-app-bar-nav-icon> -->
            <v-app-bar-title > 
                {{title}} 
                <v-icon icon="mdi-noodles"></v-icon>
            </v-app-bar-title>
            <v-btn icon="mdi-account" ></v-btn>
        </v-toolbar>
    </v-layout>
</template>

<style scoped>
</style>