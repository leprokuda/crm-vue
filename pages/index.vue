<template>

  <div class="crm">

    <div class="crm__header">
      <CrmHeader
        :title="currentPage"
      />
    </div>
    <div class="crm__body">

      <div class="crm__menu">
        <CrmMenu
          :current-page="currentPage"
          :menu-items='menuItems'
          v-on:change-page="currentPage = $event"
        />
      </div>
      <div class="crm__content">
        <CrmContent
          :title="currentPage"
        />
      </div>

    </div>

  </div>

</template>

<script lang="ts">

import CrmHeader from "@/components/CrmHeader.vue";
import CrmMenu from "@/components/CrmMenu.vue";
import CrmContent from "@/components/CrmContent.vue";

export default {

  name: 'IndexPage',
  data() {
    return {
      currentPage: 'Рабочий стол',
      menuItems: [
        {id: 1, title: 'Рабочий стол', icon: 'DeskIcon', path: '/desk', class: 'item__desk'},
        {id: 2, title: 'Администрирование', icon: 'AdministrationIcon', path: '/admin', class: 'item__admin'},
        {id: 3, title: 'Кадровый учет', icon: 'PersonnelAccountingIcon', path: '/personnel', class: 'item__personnel'},
        {id: 4, title: 'Подбор персонала', icon: 'RecruitmentIcon', path: '/recruitment', class: 'item__recruitment'},
        {id: 5, title: 'Конструктор ботов', icon: 'BotConstructorIcon', path: '/constructor', class: 'item__constructor'},
        {id: 6, title: 'Интернет-магазин', icon: 'OnlineStoreIcon', path: '/store', class: 'item__store'},
        {id: 7, title: 'Оплаты', icon: 'PaymentsIcon', path: '/payments', class: 'item__payments'},
        {id: 8, title: 'Общение', icon: 'CommunicationIcon', path: '/communication', class: 'item__communicate'},
        {id: 9, title: 'Парсеры и боты', icon: 'ParsersBotsIcon', path: '/parsers', class: 'item__parsers'},
        {id: 10, title: 'Статистика', icon: 'AnalyticsIcon', path: '/analytics', class: 'item__analytics'},
        {id: 11, title: 'Мой кабинет', icon: 'MyOfficeIcon', path: '/office', class: 'item__office'},
      ],
    }
  },

}

</script>

<style lang="scss">

  * {
    margin: 0;
    padding: 0;
    list-style: none;
    line-height: 1;
    font-size: 14px;
    text-decoration: none;
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
