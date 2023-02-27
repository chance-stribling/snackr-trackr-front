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
            <v-app-bar-title > {{title}}  <router-link to="/"> <v-icon icon="mdi-noodles"></v-icon> </router-link>  </v-app-bar-title>
        </v-toolbar>
    </v-layout>
</template>

<style scoped>
</style>