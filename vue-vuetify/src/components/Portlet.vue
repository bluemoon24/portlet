<script setup lang="ts">
import { reactive } from 'vue'

defineProps<{
  msg: string
}>()

const config = reactive({
  noheader: false,
  nomenu: true,
  pid: 'gallery-barchart-simple-roi-chart',
})

const items = reactive([
  'gallery-barchart-simple-roi-chart',
  'gallery-barchart-simple-waterfall',
  'gallery-timeline-scrolling',
  'gallery-scatter-matrix',
  'gallery-worldmap',
  'gallery-leaflet-routes',
])
</script>

<template>
  <div>
    <v-card class="portlet-container">
      <v-card-title class="text-center">{{ msg }}</v-card-title>

      <v-toolbar density="compact" color="grey-lighten-4">
        <v-checkbox
          v-model="config.noheader"
          label="noheader"
          hide-details
          density="compact"
          color="primary"
        />
        <v-checkbox
          v-model="config.nomenu"
          label="nomenu"
          hide-details
          density="compact"
          color="primary"
        />
        <v-select
          v-model="config.pid"
          :items="items"
          label="Select an example"
          hide-details
          density="compact"
          variant="outlined"
          style="min-width: 150px; margin-left: 16px"
        />
      </v-toolbar>

      <v-card class="portlet-content" variant="outlined">
        <portlet-ce :noheader="config.noheader" :pid="config.pid" height="600px"></portlet-ce>
      </v-card>
    </v-card>
  </div>
</template>

<style scoped>
.portlet-container {
  width: 100%;
  height: 100%;
  min-height: 600px;
  display: flex;
  flex-direction: column;
}

/* Visible border around portlet-ce */
.portlet-content {
  margin: 8px;
  flex: 1;
  border: 2px solid rgba(0, 0, 0, 0.2) !important;
  width: calc(100% - 16px);
}
</style>
