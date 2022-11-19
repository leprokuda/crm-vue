<template>

  <div class="crm">

    <div class="crm__header">
      <CrmHeader/>
    </div>
    <div class="crm__body">

      <div class="crm__menu">
        <CrmMenu/>
      </div>
      <div class="crm__content">
        <CrmContent/>
      </div>

    </div>

  </div>

</template>

<script lang="ts">

import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage'
})

</script>

<style lang="scss">

  * {
    margin: 0;
    padding: 0;
    list-style: none;
    line-height: 1;
    font-size: 14px;
    text-decoration: none;
    color: #0C1821;
  }

  .crm {
    width: 1366px;
    margin: auto;
    padding: 10px 20px 30px 40px;
    background: #A8CAD5;
  }

  .crm__header .header__menu {
    width: 999px;
  }

  .crm__body {
    display: flex;
    justify-content: space-between;
    padding-top: 20px;
  }

  .crm__menu {
    width: 277px;
  }

  .crm__content {
    width: 1041px;
    height: 648px;
  }

</style>
