<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <!-- Day 1 -->
        <v-expansion-panels>
          <v-expansion-panel title="Round 1: 8h30-11h30 - Mission J">
            <v-expansion-panel-text>
              <MissionDetails mission-index="j"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

          <v-expansion-panel title="11h30-12h30 - Pause Repas" readonly expand-icon="mdi-food">
          </v-expansion-panel>

          <v-expansion-panel title="Round 2: 12h30-15h30 - Mission B">
            <v-expansion-panel-text>
              <MissionDetails mission-index="b"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

          <v-expansion-panel title="Round 3: 15h40-18h40 - Mission C">
            <v-expansion-panel-text>
              <MissionDetails mission-index="c"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-col>

      <v-col cols="12">
        <!-- Day 2 -->
        <v-expansion-panels>
          <v-expansion-panel title="Round 4: 8h30-11h30 - Mission L">
            <v-expansion-panel-text>
              <MissionDetails mission-index="l"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

          <v-expansion-panel title="11h30-12h30 - Pause Repas" readonly expand-icon="mdi-food">
          </v-expansion-panel>

          <v-expansion-panel title="Round 5: 12h30-15h30 - Mission H">
            <v-expansion-panel-text>
              <MissionDetails mission-index="h"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

        </v-expansion-panels>
      </v-col>

      <v-col cols="12" sm="6">
        <v-card title="Doubles 40k">
          <v-btn class="ma-2" color="blue" prepend-icon='mdi-open-in-new' text='Guide du Joueur'
            href="https://docs.google.com/document/d/1DhAmmLNXc4_iiq2xmziNc4daed8Mbcxc/edit?usp=sharing&ouid=116957720558925974360&rtpof=true&sd=true"></v-btn>
          <v-btn class="ma-2" color="red" prepend-icon='mdi-sword' text='BCP'
            href="https://www.bestcoastpairings.com/event/9BQ5LMDAJH"></v-btn>
        </v-card>
      </v-col>

      <v-col cols="12" sm="6">
        <v-card title="Singles 40k">
          <v-btn class="ma-2" color="blue" prepend-icon='mdi-open-in-new' text='Guide du Joueur'
            href="https://docs.google.com/document/d/1QBfJ2yplm8uclDQIdazjqZtnKzL6D-77/edit?usp=sharing&ouid=116957720558925974360&rtpof=true&sd=true"></v-btn>
          <v-btn class="ma-2" color="red" prepend-icon='mdi-sword' text='BCP'
            href="https://www.bestcoastpairings.com/event/MYPQGGCKCA"></v-btn>
          <v-btn text="Grille d'évaluation de peinture" class="ma-2" color="pink" prepend-icon='mdi-brush-outline'
            href="https://docs.google.com/forms/d/e/1FAIpQLScJT49vHxb3lxBGKVCYden85MItRbbD2SuJpVzuYYylY_aCsw/viewform?usp=sharing"></v-btn>
        </v-card>
      </v-col>

      <v-col cols="12" sm="6">
        <v-card title="AR Layouts WTC" subtitle="Déploiement en réalité augmentée">
          <v-btn text="Android" class="ma-2" color="green" prepend-icon='mdi-android'
            href="https://play.google.com/store/apps/details?id=com.ARLayoutsWTC.ARLayoutsWTC"></v-btn>
          <v-btn text="Apple" class="ma-2" color="blue" prepend-icon='mdi-apple'
            href="https://apps.apple.com/us/app/ar-layouts-wtc/id6499312368"></v-btn>
        </v-card>
      </v-col>

      <v-col cols="12" sm="6">
        <v-card title="WTC FAQs & Downloads">
          <v-btn text="WTC Downloads" class="ma-2" color="orange" prepend-icon='mdi-open-in-new'
            href="https://worldteamchampionship.com/wtc-rules/"></v-btn>
        </v-card>
      </v-col>

      <v-col cols="12" sm="6">
        <v-card title="Age of Sigmar">
          <v-btn text="Grille d'évaluation de peinture" class="ma-2" color="pink" prepend-icon='mdi-brush-outline'
            href="https://docs.google.com/forms/d/e/1FAIpQLSecILbgzWpvLXx69wdqHJO6OQS2SRW3KoK7xt4rnDJhdvysKw/viewform?usp=header"></v-btn>
        </v-card>
      </v-col>
    </v-row>

  </v-container>
</template>

<script setup>
//
</script>
