<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import Portlet from './components/Portlet.vue'
</script>

<template>
  <v-app>
    <v-container class="pa-6" style="max-width: 1400px">
      <div class="custom-row">
        <!-- Left Column -->
        <div class="custom-col">
          <v-card class="pa-6 left-panel" elevation="2">
            <div class="text-center">
              <img
                alt="Viz-it logo"
                class="logo"
                src="./assets/viz-it.svg"
                width="250"
                height="250"
              />

              <div class="wrapper">
                <HelloWorld msg="You did it!" />
              </div>
            </div>
          </v-card>
        </div>

        <!-- Right Column -->
        <div class="custom-col">
          <v-card class="pa-6 right-panel" elevation="2">
            <Portlet msg="Welcome to your Portlet App" />
          </v-card>
        </div>
      </div>
    </v-container>
  </v-app>
</template>

<style scoped>
.custom-row {
  display: flex;
  gap: 24px;
  flex-wrap: wrap;
}

.custom-col {
  flex: 1;
  min-width: 300px;
}

.left-panel {
  background: #ffffff;
  border-radius: 8px;
  width: 100%;
  height: auto;
}

.right-panel {
  background: #f8f8f8;
  border-radius: 8px;
  width: 100%;
  height: auto;
  display: block;
  overflow: hidden;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

.wrapper {
  display: flex;
  place-items: center;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}

/* Responsive behavior */
@media (max-width: 768px) {
  .custom-row {
    flex-direction: column;
  }

  .custom-col {
    flex: none;
  }
}
</style>
