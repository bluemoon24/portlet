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
    <q-card class="portlet-container">
      <q-card-section class="text-center">
        <div class="text-h6">{{ msg }}</div>
      </q-card-section>

      <q-toolbar class="bg-grey-2">
        <q-checkbox v-model="config.noheader" label="noheader" color="primary" dense />
        <q-checkbox v-model="config.nomenu" label="nomenu" color="primary" dense class="q-ml-md" />
        <q-select
          v-model="config.pid"
          :options="items"
          label="Select an example"
          outlined
          dense
          style="min-width: 150px"
          class="q-ml-md"
        />
      </q-toolbar>

      <q-card class="portlet-content" bordered>
        <portlet-ce :noheader="config.noheader" :pid="config.pid" height="600px"></portlet-ce>
      </q-card>
    </q-card>
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
