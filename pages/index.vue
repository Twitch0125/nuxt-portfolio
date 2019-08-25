<template>
  <v-layout column justify-center align-center>
    <h1 class="text-center headline mb-6">My Work</h1>
    <v-container fluid xs12 sm8 md6>
      <v-row align="center" justify="center">
        <v-col cols="9">
          <v-row align="center" justify="center" style="height: 300px">
            <v-card :key="i+1" v-for="(thing, i) in things" class="ma-4">
              <v-row class="pl-4">
                <v-col class="shrink">
                  <v-img
                    height="200"
                    width="200"
                    src="https://cdn.vuetifyjs.com/images/cards/store.jpg"
                  ></v-img>
                </v-col>
                <v-col class="text-center">
                  <v-container class="pa-0">
                    <v-row>
                      <v-col class="mx-2">
                        <v-card-text>text goes here for descriptionstext goes here for descriptionstext goes here for descriptionstext goes here for descriptions</v-card-text>
                      </v-col>
                    </v-row>
                  </v-container>
                </v-col>
              </v-row>
            </v-card>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </v-layout>
</template>

<style>
.myWrap {
  overflow-wrap: break-word;
}
</style>

<script>
export default {
  data() {
    return {
      things: [{}, {}, {}, {}, {}, {}]
    };
  },
  components: {}
};
</script>
