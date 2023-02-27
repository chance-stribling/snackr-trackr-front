<script lang="ts">
import {defineComponent} from 'vue'

export default defineComponent({
    data() {
        return{
            title: "Snackr Trackr",
            snacks:[
                {name: 'Sprite',calories:140,sugar:38,count:2},
                {name: 'Sprite',calories:140,sugar:38,count:2},
                {name: 'Sprite',calories:140,sugar:38,count:2},
                {name: 'Sprite',calories:140,sugar:38,count:2},
                {name: 'Sprite',calories:140,sugar:38,count:2},
                {name: 'Sprite',calories:140,sugar:38,count:2},
                {name: 'Sprite',calories:140,sugar:38,count:2},
                {name: 'Sprite',calories:140,sugar:38,count:2},
                {name: 'Sprite',calories:140,sugar:38,count:2},
                {name: 'Sprite',calories:140,sugar:38,count:2},
                {name: 'Sprite',calories:140,sugar:38,count:2},
            ],
        }
    }
})
</script>

<template>
    <v-layout>
        <v-card 
            width="500px"
            height="510px"
            class="mx-auto mt-15"
        >
            <v-card-title>All Snacks</v-card-title>
            <v-table
                fixed-header
                height="400px"
            >
                <thead>
                    <tr>
                        <th>Snack</th>
                        <th>Calories</th>
                        <th>Sugar</th>
                        <th>Count</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="snack in snacks" :key="snack.name">
                        <td>{{ snack.name }}</td>
                        <td>{{ snack.calories }}</td>
                        <td>{{ snack.sugar }}</td>
                        <td>{{ snack.count }}</td>
                    </tr>
                </tbody>
            </v-table>
            <v-card-actions>
                <v-btn class="mx-auto" variant="tonal">Have a Snack</v-btn>
            </v-card-actions>
        </v-card>
    </v-layout>
</template>

<style>
</style>