<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <!-- Day 1 -->
        <v-expansion-panels>
          <v-expansion-panel title="Round 1: 8h30-12h00 - Mission H">
            <v-expansion-panel-text>
              <MissionDetails mission-index="h"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

          <v-expansion-panel title="12h00-12h45 - Pause Repas" readonly expand-icon="mdi-food">
          </v-expansion-panel>

          <v-expansion-panel title="Round 2: 12h45-16h15 - Mission N">
            <v-expansion-panel-text>
              <MissionDetails mission-index="n"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

          <v-expansion-panel title="Round 3: 16h30-20h00 - Mission P">
            <v-expansion-panel-text>
              <MissionDetails mission-index="p"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-col>

      <v-col cols="12">
        <!-- Day 2 -->
        <v-expansion-panels>
          <v-expansion-panel title="Round 4: 8h30-12h00 - Mission J">
            <v-expansion-panel-text>
              <MissionDetails mission-index="j"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

          <v-expansion-panel title="12h00-12h45 - Pause Repas" readonly expand-icon="mdi-food">
          </v-expansion-panel>

          <v-expansion-panel title="Round 5: 12h45-16h15 - Mission L">
            <v-expansion-panel-text>
              <MissionDetails mission-index="l"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

        </v-expansion-panels>
      </v-col>

      <v-col cols="12" sm="6">
        <v-card title="Grande Croisade">
          <v-btn class="ma-2" color="blue" prepend-icon='mdi-open-in-new' text='Guide du Joueur'
            href="https://docs.google.com/document/d/1wMdCLVwi3h_fLRR68ySf8lQumdlTvE8R/edit?usp=sharing&ouid=116957720558925974360&rtpof=true&sd=true"></v-btn>
          <v-btn class="ma-2" color="red" prepend-icon='mdi-sword' text='BCP'
            href="https://www.bestcoastpairings.com/event/ErEW0z3h9ZWl"></v-btn>
          <v-btn text="Grille d'évaluation de peinture" class="ma-2" color="pink" prepend-icon='mdi-brush-outline'
            href="https://docs.google.com/forms/d/e/1FAIpQLSdQ4U__hBlHElhCcB30RkuUr7NQShOIUTNYKlKwjsqY6yAcBA/viewform?usp=dialog"></v-btn>
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
