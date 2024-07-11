<script>
export default {
  props: {
    tags: {
      type: Array,
      required: true,
    },
    alignment: {
      type: String,
      default: 'left',
    },
    maxWidth: {
      type: String,
      default: '100%',
    },

  },
}
</script>

<template>
  <div
    :class="['tag-list', {'tag-list_align_left': alignment === 'left', 'tag-list_align_width': alignment === 'width'}]"
    :style="{ maxWidth: maxWidth }">
    <div v-for="(tag, index) in tags" :key="index" class="tag-list__item">
      <span>{{ tag.text }}</span>
      <v-icon v-if="tag.icon" :size="16">
        {{ tag.icon }}
      </v-icon>
      <v-icon v-if="index < tags.length - 1" :size="16">
        mdi-circle-small
      </v-icon>
    </div>
  </div>
</template>

<style lang="scss" scoped src="./taglist.scss"></style>
