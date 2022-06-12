<template>
  <v-col cols="12" :style="{ transform: image? 'translateY(-25px)' : '' }">
    <v-avatar
      size="150"
      style="transform: translateY(25px); z-index: 5"
      v-if="image"
    >
      <v-img src="@/assets/cardPicture/PersonalPicture.png"/>
    </v-avatar>
    <v-card outlined style="border-radius: 15px" :color="color">
      <v-row class="mt-1 mb-0">
        <v-col
          :class="{
            'mx-6 ': true,
            'my-0': !image,
            'py-0': true,
            'mt-6': image,
          }"
          :style="{ marginTop: image ? '50px !important;' : '' }"
        >
          <!-- class="mx-6 my-0 py-0" -->
          <span class="font-weight-bold" :style="{ color: title.color }">
            {{ title.message }}
          </span>
        </v-col>
      </v-row>
      <div v-for="(element, index) in message" :key="index">
        <v-row v-if="subHeader" :class="{ 'mt-2': subHeader[index] }">
          <v-col class="mx-6 my-0 py-0">
            <span class="text-caption font-weight-bold">
              {{ subHeader[index] }}
            </span>
          </v-col>
        </v-row>
        <v-row class="mt-0">
          <v-col class="mx-6 my-0">
            <span class="text-caption font-weight-light"  :style="{color: subHeader ? '#757575': 'white'}">
              {{ message[index] }}
            </span>
          </v-col>
        </v-row>
      </div>
      <div v-for="(bullet, index) in bullets" :key="index" class="mb-2">
        <v-row class="mt-2">
          <v-col class="mx-6 my-0 py-0">
            <span class="text-caption font-weight-bold">
              {{ bullet.title }}
            </span>
          </v-col>
        </v-row>
        <v-row class="mx-0 py-0" v-for="(element, index) in bullet.message " :key="index">
          <v-col class="mx-6 my-0 py-0">
            <span class="text-caption font-weight-light">
              &#8226; {{ element }}
            </span>
          </v-col>
        </v-row>
      </div>
    </v-card>
  </v-col>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class CurriculumCard extends Vue {
  @Prop() private color!: string;
  @Prop() private image!: string;
  @Prop() private title!: Record<string, unknown>;
  @Prop() private subHeader!: [];
  @Prop() private message!: [];
  @Prop() private bullets!: Record<string, unknown>;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>