<template>
  <v-col cols="12">
    <v-card outlined style="border-radius: 15px;">
      <v-row class="mt-1 mb-0">
        <v-col class="mx-6 my-0 py-0"> 
          <span class="" style="color: #FF5722;">
            {{ title }}
          </span> 
          </v-col>
      </v-row>
      <v-row v-if="subHeader" class="my-0">
        <v-col class="mx-6 my-0 py-0">
          <span class="text-subtitle-2">
            {{ subHeader }}
          </span>
        </v-col>
      </v-row>
      <v-row class="my-0">
        <v-col class="mx-6 my-0 py-0">
          <span class="text-caption font-weight-light">
            {{ message }}
          </span>
        </v-col>
      </v-row>
    </v-card>
  </v-col>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class CurriculumCard extends Vue {
  @Prop() private title!: string;
  @Prop() private subHeader!: string;
  @Prop() private message!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
