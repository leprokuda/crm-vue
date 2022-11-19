<template>

  <nav id="menu" class="menu" v-bind:class="active" v-on:click.prevent>

    <CrmMenuItem/>

  </nav>

</template>

<script lang="ts">

export default {
  name: 'CrmMenu',

  // data() {
  //   return {
  //     active: 'item__desk',
  //   }
  // },
  // methods: {
  //   makeActive: function(item: string){
  //     this.active = item;
  //   }
  // }
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

  .menu__item {
    display: flex;
    align-items: center;
    padding: 12px 30px;
  }

  .menu__item svg {
    padding-right: 30px;
  }

  // ================== Стили ссылок ===================

  .active {
    color: #FFFFFF;
  }

  .nuxt-link-active {
    color: #0C1821;
  }

  //.nuxt-link-active:active {
  //  color: #FFFFFF;
  //}

  // ====================== Стили активных пунктов меню =========================

  nav.item__desk .item__desk li {
    background: #2274A5;
  }

  .item__admin li {
    background: #1E892F;
  }

  nav.item__personnel .item__personnel li {
    background: #741E89;
  }

  nav.item__recruitment .item__recruitment li {
    background: #891E4B;
  }

  nav.item__constructor .item__constructor li {
    background: #CF9603;
  }

  nav.item__store .item__store li {
    background: #894f03;
  }

  nav.item__payments .item__payments li {
    background: #ac1a03;
  }

  nav.item__communicate .item__communicate li {
    background: #05514c;
  }

  nav.item__parsers .item__parsers li {
    background: #3d2486;
  }

  nav.item__analytics .item__analytics li {
    background: #143c36;
  }

  nav.item__office .item__office li {
    background: #668d2a;
  }





</style>
