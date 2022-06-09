<template>
  <div>
    <center>
      <v-row class="mt-5" style="max-width: 700px; background-color: #ECEFF1;">
        <v-col cols="12" sm="4" md="4">
          <CurriculumCard
            title="Juan De Dios Reynosa Silva"
            message="Software Developer"
          />
          <CurriculumCard title="How to reach me" message="" />
          <CurriculumCard
            title="Personal interests"
            message="Artificial Intelligence.
              Data science.
              Machine learning.
              Internet Of Things.
              Mobile software."
          />
        </v-col>
        <v-col cols="12" sm="4" md="4">
          <CurriculumCard
            title="Personal Profile"
            message="I am a Computer Science 
              Engineer with robust problem solving skills and proven experience in creating 
              and designing software.
              "
          />
          <CurriculumCard
            title="Education"
            subHeader="Universidad Autónoma de Ciudad Juárez"
            message="Bachelor's degree in Computer Science (2016-2021)."
          />
          <CurriculumCard
            title="Professional summary"
            subHeader="Network technician in UACJ 
              (2019)."
            message="Maintenance and installation of structured network 
              and basic network management of switches and routers."
          />
        </v-col>
        <v-col cols="12" sm="4" md="4">
          <CurriculumCard title="Skills" message="message" />
          <CurriculumCard title="Lenguages" message="message" />
        </v-col>
      </v-row>
    </center>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import CurriculumCard from "@/components/CurriculumCard.vue"; // @ is an alias to /src

@Component({
  components: {
    CurriculumCard,
  },
})
export default class Home extends Vue {}
</script>
