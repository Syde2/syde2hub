<script setup>
import {ref} from 'vue'
const leftDrawerOpen = ref(false)
</script>


<template>
  <q-layout view="lHh Lpr lFf" class="bg-dark" >
    <q-header class="bg-dark">
      <q-toolbar>

        <q-toolbar-title>
          <p class="text-h4 text-white my-font q-pa-sm"> 師 </p>
        </q-toolbar-title>

        
      </q-toolbar>
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

