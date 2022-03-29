<template>
  <div :class="classes">
    <TheSearch
      :search-query="searchQuery"
      @update-search-query="$emit('update-search-query', $event)"
    />
    <BaseTooltip text="Search with your voice">
      <button class="p-2 focus:outline-none">
        <BaseIcon name="microphone" class="w-5 h-5" /></button
    ></BaseTooltip>
  </div>
</template>

<script>
import TheSearch from './TheSearch.vue';
export default {
  components: { TheSearch, BaseTooltip, BaseIcon },
  props: ['searchQuery'],
  emits: ['update-search-query'],
};
</script>

<style lang="scss" scoped></style>
