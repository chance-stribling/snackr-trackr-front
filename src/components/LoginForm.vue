<script lang="ts">
import {defineComponent} from 'vue'

export default defineComponent({
   data() {
     return{
       form: false,
       email: null,
       password: null,
       loading: false
      }
    }

  })
</script>

<template>
    <v-layout>
    <v-card
    width="500px"
    height="450px"
    class="mx-auto mt-15 " 
    >
        <v-form
        v-model="form"
        >
            <v-card-title >Login</v-card-title>
            <v-text-field
                v-model="email"
                class="mb-2"
                clearable
                label="Email"

            ></v-text-field>
            <v-text-field
                v-model="password"
                clearable
                label="Password"
            ></v-text-field>
            <v-card-actions class="justify-space-evenly">
              <v-btn to="/snacks">Login</v-btn>
              <v-btn rounded="outlined" color="black">Register</v-btn>
            </v-card-actions>
            </v-form>
        </v-card>
    </v-layout>
      
</template>