<template>
  <v-card max-width="600" :hover="hover" class="ma-4">
    <v-row class="pl-4">
      <v-col class="shrink">
        <v-img height="200" width="200" :src="image"></v-img>
      </v-col>
      <v-col class="text-center">
        <v-container class="pa-0">
          <v-row>
            <v-col class="mx-2">
              <v-card-text v-text="description"></v-card-text>
            </v-col>
          </v-row>
          <v-row>
            <v-col class="mx-2">
              <v-card-actions>
                <v-btn :target="target" depressed :href="github" color="secondary">
                  Github
                  <v-icon>mdi-github-circle</v-icon>
                </v-btn>
                <v-btn
                  v-if="project"
                  :href="project"
                  :target="target"
                  text
                  color="accent"
                >View Project</v-btn>
              </v-card-actions>
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
    return {
      hover: true,
      target: "new"
    };
  },
  props: {
    image: String,
    description: String,
    github: String,
    project: String
  }
};
</script>