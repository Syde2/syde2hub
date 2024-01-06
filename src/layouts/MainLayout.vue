<script setup>
import {ref} from 'vue'
const leftDrawerOpen = ref(false)
</script>


<template>
  <q-layout view="lHh Lpr lFf" class="bg-dark" >
    <q-header class="bg-dark">
      <q-toolbar>

        <q-toolbar-title>
          <q-btn  label="師" flat to="/" :ripple="false" size="xl"  round /> 
        </q-toolbar-title>

        
      </q-toolbar>
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<style>


</style>