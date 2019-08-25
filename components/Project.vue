<template>
  <v-card class="ma-4">
    <v-row class="pl-4">
      <v-col class="shrink">
        <v-img height="200" width="200" :src="image"></v-img>
      </v-col>
      <v-col class="text-center">
        <v-container class="mx-2">
          <v-row>
            <v-col>
              <p>text goes here</p>
            </v-col>
          </v-row>
        </v-container>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: {
    image: string
  }
};
</script>