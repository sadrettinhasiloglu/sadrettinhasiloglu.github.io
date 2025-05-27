<template>
  <v-container fluid>
    <v-row>
      <v-col cols="12" md="6">
        <v-row dense>
          <v-col v-for="(variant, i) in variants" :key="i" cols="12">
            <v-card class="d-flex" :color="color[i]" variant="tonal">
              <template v-slot:prepend>
                <v-icon :color="color[i]" icon="mdi-tree" />
              </template>
              <v-card-item>
                <div>
                  <div class="text-overline mb-1">{{ variant }}</div>
                  <div class="text-h6 mb-1">value</div>
                  <div class="text-caption">description</div>
                </div>
              </v-card-item>
            </v-card>
          </v-col>
        </v-row>
      </v-col>

      <v-col class="d-flex" cols="12" md="6">
        <v-card class="flex-grow-1" color="grey" variant="tonal">
          <v-card-item>
            <div>
              <div class="text-overline mb-1">En yüksek bağışçılar</div>
              <div class="text-h6 mb-1">value</div>
              <div class="text-caption">description</div>
            </div>
          </v-card-item>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import { ref } from "vue";

const variants = ["Bağışlanan Fidan", "Toplam Bağışçı Sayısı"];
const color = ["green", "blue"];
</script>
