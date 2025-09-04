<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <!-- Day 1 -->
        <v-expansion-panels>
          <v-expansion-panel title="Round 1: 8h30-12h00 - Mission C">
            <v-expansion-panel-text>
              <MissionDetails mission-index="c"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

          <v-expansion-panel title="12h00-13h15 - Pause Repas" readonly expand-icon="mdi-food">
          </v-expansion-panel>

          <v-expansion-panel title="Round 2: 13h15-16h45 - Mission O">
            <v-expansion-panel-text>
              <MissionDetails mission-index="o"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

          <v-expansion-panel title="Round 3: 17h00-20h30 - Mission G">
            <v-expansion-panel-text>
              <MissionDetails mission-index="g"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-col>

      <v-col cols="12">
        <!-- Day 2 -->
        <v-expansion-panels>
          <v-expansion-panel title="Round 4: 8h30-12h00 - Mission F">
            <v-expansion-panel-text>
              <MissionDetails mission-index="f"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

          <v-expansion-panel title="12h00-13h15 - Pause Repas" readonly expand-icon="mdi-food">
          </v-expansion-panel>

          <v-expansion-panel title="Round 5: 13h15-16h45 - Mission L">
            <v-expansion-panel-text>
              <MissionDetails mission-index="l"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

        </v-expansion-panels>
      </v-col>

      <v-col cols="12" sm="6">
        <v-card title="TEIL">
          <v-btn class="ma-2" color="blue" prepend-icon='mdi-open-in-new' text='Guide du Joueur'
            href="404"></v-btn>
          <v-btn class="ma-2" color="red" prepend-icon='mdi-sword' text='BCP'
            href="https://www.bestcoastpairings.com/event/wf32USYfefge"></v-btn>
          <v-btn text="Grille d'évaluation de peinture" class="ma-2" color="pink" prepend-icon='mdi-brush-outline'
            href="404"></v-btn>
          <v-btn class="ma-2" color="purple" prepend-icon='mdi-play' text='Pairing Demo'
            href="https://www.youtube.com/watch?v=2eiKPZ0sfPw"></v-btn>
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
    </v-row>

  </v-container>
</template>

<script setup>
//
</script>
