<template>
  <div>
    <center>
      <v-row class="mt-0" style="max-width: 760px; background-color: #eceff1">
        <v-col cols="12" sm="4" md="4" class="mt-2">
          <CurriculumCard
            image="@/assets/cardPicture/PersonalPicture.png"
            color="#FF5722"
            :title="{
              message: 'Juan De Dios Reynosa Silva',
              color: 'white',
            }"
            :message="['Software Developer']"
          />
          <CurriculumCard
            :title="{
              message: 'How to reach me',
              color: '#FF5722',
            }"
            :subHeader="['Cellphone', 'E-mail', 'LinkedIn', 'GitHub']"
            :message="['656-789-2980', 'jreynosa.developer@gmail.com', 'https://www.linkedin.com/in/juan-de-dios-reynosa-silva-429018202/', 'https://github.com/Notbrynal']"
          />
          <CurriculumCard
            :title="{
              message: 'Personal interests',
              color: '#FF5722',
            }"
            :subHeader="['Computer Science']"
            :message="[
              'Artificial Intelligence. Data science. Machine learning. Internet Of Things. Mobile software.',
            ]"
          />
        </v-col>
        <v-col cols="12" sm="4" md="4" class="mt-2">
          <CurriculumCard
            :title="{
              message: 'Personal Profile',
              color: '#FF5722',
            }"
            :subHeader="['About me']"
            :message="[
              'I am a Computer Science Engineer with robust problem solving skills and proven experience in creating and designing software.',
            ]"
          />
          <CurriculumCard
            :title="{
              message: 'Education',
              color: '#FF5722',
            }"
            :subHeader="['Universidad Autónoma de Ciudad Juárez']"
            :message="['Bachelors degree in Computer Science (2016-2021).']"
          />
          <CurriculumCard
            :title="{
              message: 'Professional summary',
              color: '#FF5722',
            }"
            :subHeader="[
              'Software developer in United DevOps (2020).',
              'Software developer in Stoneridge (2021-present).',
            ]"
            :message="[
              'Landing web page for a health care company and administration suite for itself maintainance.',
              'Full stack developer of web software based on Lean Manufacturing Operational Systems, Visual Management and Business Intelligence.',
            ]"
          />
        </v-col>
        <v-col cols="12" sm="4" md="4" class="mt-2">
          <CurriculumCard
            :title="{
              message: 'Skills',
              color: '#FF5722',
            }"
            :bullets="
            [
              {
                title: 'Technical skills',
                message: [
                  'C#',
                  'Python',
                  'TypeScript',
                  'Vuetify',
                  'VueJS',
                  'Git',
                  'Azure Data Studio',
                  'SMSS',
                  'Microsoft SQL Server',
                  'Design Patterns',
                  'SCRUM',
                ]
              },
              {
                title: 'Soft skills',
                message: [
                  'Teamwork',
                  'Communication',
                  'Problem solving',
                  'Adaptability',
                  'Time management',
                  'Organization',
                  'Creativity',
                  'Initiative',
                  'Self-learning',
                  'Decision making',
                ]
              }
            ]
            "
          />
          <CurriculumCard
            :title="{
              message: 'Lenguages',
              color: '#FF5722',
            }"
            :subHeader="['Spanish', 'English']"
            :message="['Native speaker.', 'Advanced writing, reading and speaking. TOEFL ITP Test Score: 545 points.']"
          />
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
