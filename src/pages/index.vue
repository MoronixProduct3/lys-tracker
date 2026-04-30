<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <!-- Day 1 -->
        <v-expansion-panels>
          <v-expansion-panel title="Round 1: 8h30-11h30 - Mission G">
            <v-expansion-panel-text>
              <MissionDetails mission-index="g"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

          <v-expansion-panel title="11h30-12h30 - Pause Repas" readonly expand-icon="mdi-food">
          </v-expansion-panel>

          <v-expansion-panel title="Round 2: 12h30-15h30 - Mission O">
            <v-expansion-panel-text>
              <MissionDetails mission-index="o"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

          <v-expansion-panel title="Round 3: 15h40-18h40 - Mission J">
            <v-expansion-panel-text>
              <MissionDetails mission-index="j"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-col>

      <v-col cols="12">
        <!-- Day 2 -->
        <v-expansion-panels>
          <v-expansion-panel title="Round 4: 8h30-11h30 - Mission A">
            <v-expansion-panel-text>
              <MissionDetails mission-index="a"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

          <v-expansion-panel title="11h30-12h30 - Pause Repas" readonly expand-icon="mdi-food">
          </v-expansion-panel>

          <v-expansion-panel title="Round 5: 12h30-15h30 - Mission F">
            <v-expansion-panel-text>
              <MissionDetails mission-index="f"></MissionDetails>
            </v-expansion-panel-text>
          </v-expansion-panel>

        </v-expansion-panels>
      </v-col>

      <v-col cols="12" sm="6">
        <v-card title="TEIL">
          <v-btn class="ma-2" color="blue" prepend-icon='mdi-open-in-new' text='Guide du Joueur'
            href="https://docs.google.com/document/d/10Qz4gic10sdJCkHcZdkFnjEuUHC8vGum/edit?usp=sharing&ouid=116957720558925974360&rtpof=true&sd=true"></v-btn>
          <v-btn class="ma-2" color="orange" prepend-icon='mdi-sword' text='BCP'
            href="https://www.bestcoastpairings.com/event/nU8Ddx55eYbA"></v-btn>
          <v-btn class="ma-2" color="red" prepend-icon='mdi-play' text='Video Intro'
            href="https://youtu.be/y4m_3NUuyN4"></v-btn>
          <v-btn class="ma-2" color="teal" prepend-icon='mdi-brush' text='Auto-Evaluation Hobby'
            href="https://docs.google.com/forms/d/e/1FAIpQLSfu1Q7qoW323NL6G7mur46f7JQ9Fgs2A9xYa6oLZPXUU7ih-A/viewform?usp=publish-editor"></v-btn>
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
            href="https://wtc-belgium.com/wh40k-rules/"></v-btn>
        </v-card>
      </v-col>
    </v-row>

  </v-container>
</template>

<script setup>
//
</script>
