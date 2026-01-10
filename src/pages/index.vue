<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <!-- Day 1 -->
        <v-expansion-panels>
          <v-expansion-panel title="Round 1: 8h30-12h00 - Mission O">
            <v-expansion-panel-text>
              <MissionDetails mission-index="o"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

          <v-expansion-panel title="12h00-13h00 - Pause Repas" readonly expand-icon="mdi-food">
          </v-expansion-panel>

          <v-expansion-panel title="Round 2: 13h00-16h30 - Mission C">
            <v-expansion-panel-text>
              <MissionDetails mission-index="c"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

          <v-expansion-panel title="Round 3: 16h45-20h15 - Mission B">
            <v-expansion-panel-text>
              <MissionDetails mission-index="b"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-col>

      <v-col cols="12">
        <!-- Day 2 -->
        <v-expansion-panels>
          <v-expansion-panel title="Round 4: 8h30-12h00 - Mission I">
            <v-expansion-panel-text>
              <MissionDetails mission-index="i"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

          <v-expansion-panel title="12h00-13h00 - Pause Repas" readonly expand-icon="mdi-food">
          </v-expansion-panel>

          <v-expansion-panel title="Round 5: 13h00-16h30 - Mission E">
            <v-expansion-panel-text>
              <MissionDetails mission-index="e"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

        </v-expansion-panels>
      </v-col>

      <v-col cols="12" sm="6">
        <v-card title="TEIL">
          <v-btn class="ma-2" color="blue" prepend-icon='mdi-open-in-new' text='Guide du Joueur'
            href="https://docs.google.com/document/d/1wMdCLVwi3h_fLRR68ySf8lQumdlTvE8R/edit#heading=h.gjdgxs"></v-btn>
          <v-btn class="ma-2" color="red" prepend-icon='mdi-sword' text='BCP'
            href="https://www.bestcoastpairings.com/event/a9dk41yw4W24"></v-btn>
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
