<template>
  <v-card
    class="mx-auto"
    max-width="344"
  >
    <v-img
      :src="pic"
      height="200px"
      cover
    ></v-img>

    <v-card-title>
      {{ title }}
    </v-card-title>

    <v-card-subtitle>
      {{ description }}
    </v-card-subtitle>

    <v-card-actions>
      <v-btn
        color="info"
        variant="text"
        link
        :href="link"
      >
        Visit
      </v-btn>

      <v-spacer></v-spacer>

      <v-btn
        :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'"
        @click="show = !show"
      ></v-btn>
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

        <v-card-text>
          {{ longDescription }}
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>

import { ref } from 'vue'

export default {
  props: {
    title: String,
    description: String,
    longDescription: String,
    link: String,
    pic: String
  },
  setup() {
    const show = ref(false)

    return {
      show
    }
  },
}
</script>