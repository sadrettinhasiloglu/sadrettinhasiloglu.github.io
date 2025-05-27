<template>
  <v-container fluid>
    <v-carousel cycle height="200" hide-delimiter-background>
      <v-carousel-item v-for="(slide, i) in slides" :key="i">
        <v-sheet height="100%">
          <div class="d-flex fill-height justify-center align-center">
            <div class="text-h2">{{ slide }} message</div>
          </div>
        </v-sheet>
      </v-carousel-item>
    </v-carousel>
  </v-container>
</template>

<script setup>
const colors = ["indigo", "warning", "pink darken-2", "red lighten-1", "deep-purple accent-4"];
const slides = ["First", "Second", "Third", "Fourth", "Fifth"];
</script>
