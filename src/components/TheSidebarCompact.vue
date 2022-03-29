<template>
  <aside :class="classes">
    <section>
      <ul>
        <SidebarCompactNavItem
          v-for="navItem in navItems"
          :key="navItem.label"
          :label="navItem.label"
          :icon="navItem.icon"
          :is-active="navItem.isActive"
        />
      </ul>
    </section>
  </aside>
</template>

<script>
import BaseIcon from './BaseIcon.vue';
import SidebarCompactNavItem from './SidebarCompactNavItem.vue';
export default {
  props: {},
  data() {
    return {
      navItems: [
        { label: 'Home', icon: 'home', isActive: true },
        { label: 'Trending', icon: 'fire', isActive: false },
        { label: 'Subscriptions', icon: 'collection', isActive: false },
        { label: 'Library', icon: 'duplicate', isActive: false },
        { label: 'History', icon: 'clock', isActive: false },
      ],
    };
  },
  computed: {
    classes() {
      return [
        'min-h-screen',
        'overflow-auto',
        'fixed',
        'top-0',
        'pt-14',
        'bg-white',
        'z-20',
      ];
    },
  },
  components: { BaseIcon, SidebarCompactNavItem },
};
</script>

<style lang="scss" scoped></style>
