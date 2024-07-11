<template>
  <div class="app">
    <!-- Компонент на всю ширину экрана с выравниванием по левому краю -->
    <v-card class="app__card">
      <v-card-title class="app__card-title">Компонент на всю ширину экрана с выравниванием по левому краю</v-card-title>
      <v-card-text class="app__card-text">
        <TagList
          :tags="tags"
          alignment="left"
          :max-width="'100%'"
        />
      </v-card-text>
    </v-card>

    <!-- Компонент на всю ширину экрана с выравниванием по ширине -->
    <v-card class="app__card">
      <v-card-title class="app__card-title">Компонент на всю ширину экрана с выравниванием по ширине</v-card-title>
      <v-card-text class="app__card-text">
        <TagList
          :tags="tags"
          alignment="width"
          :max-width="'100%'"
        />
      </v-card-text>
    </v-card>

    <!-- Компонент на 50% ширины экрана с выравниванием по левому краю и по ширине -->
    <div class="app__flex-container">
      <v-card class="app__card app__card_half">
        <v-card-title class="app__card-title">Компонент на 50% ширины экрана с выравниванием по левому краю</v-card-title>
        <v-card-text class="app__card-text">
          <TagList
            :tags="tags"
            alignment="left"
            :max-width="'100%'"
          />
        </v-card-text>
      </v-card>
      <v-card class="app__card app__card_half">
        <v-card-title class="app__card-title">Компонент на 50% ширины экрана с выравниванием по ширине</v-card-title>
        <v-card-text class="app__card-text">
          <TagList
            :tags="tags"
            alignment="width"
            :max-width="'100%'"
          />
        </v-card-text>
      </v-card>
    </div>
  </div>
</template>

<script>
import TagList from '../components/taglist.vue'
import data from './index.json'

export default {
  components: { TagList },
  data() {
    return {
      tags: data
    }
  },
}
</script>

<style src="./index.scss" lang="scss" scoped></style>
