<template>

  <nav class="menu" v-bind:class="active" v-on:click.prevent>

    <ul class="menu__list">

      <div
        v-for="item in menuItems"
        v-on:click="$emit('change-page', item.title)"
      >
        <CrmMenuItem
          :current-page="currentPage"
          :key="item.id"
          :itemData="item"
        />
      </div>

    </ul>

  </nav>

</template>

<script lang="ts">

import CrmMenuItem from "@/components/CrmMenuItem.vue";

export default {
  name: 'CrmMenu',
  components: {
    CrmMenuItem,
  },
  props: ['menuItems', 'currentPage'],
  computed: {}
}

</script>

<style lang="scss">

  .menu {
    background: #FFFFFF;
    border: 1px solid #BCDFE7;
    border-radius: 10px;
    padding: 20px 0 22px 0;
  }

  .menu__list {
    font-size: 14px;
  }

  // ================== Стили ссылок ===================

  .nuxt-link-active {
    color: #0C1821;
  }

  //.nuxt-link-active:active {
  //  color: #FFFFFF;
  //}


</style>
