<script lang="ts">
import {defineComponent} from 'vue'

export default defineComponent({
    data() {
        return{
            title: "Snackr Trackr",
            dialog: false, dialog2: false,
            items: ['foo', 'bar', 'fizz', 'buzz'],
            values: 'foo',
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
            <v-card-actions class="mt-2">
                
                <v-btn class="mx-auto" variant="tonal">Have a Snack
                    <v-dialog
                        v-model="dialog"
                        activator="parent"
                        width="600px"
                    >
                        <v-card>
                            <v-card-title>What are we having?</v-card-title>
                            <v-sheet width="200px"></v-sheet>
                            
                        <v-card-actions>
                            <v-btn color="primary" block @click="dialog = false">Close Dialog</v-btn>
                        </v-card-actions>
                        </v-card>
                    </v-dialog>
                </v-btn>
                
                <v-btn class="mx-auto" variant="tonal">New Snack

                    <v-dialog
                        v-model="dialog2"
                        activator="parent"
                        width="600px"
                    >
                        <v-card>
                            <v-card-title>Create Snack</v-card-title>
                            <v-card-text>
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                        </v-card-text>
                        <v-card-actions>
                            <v-btn block @click="dialog2 = false">Close Dialog</v-btn>
                        </v-card-actions>
                        </v-card>
                    </v-dialog>
                </v-btn>
            </v-card-actions>
        </v-card>
    </v-layout>
</template>

<style scoped>

</style>