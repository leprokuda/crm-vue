<template>

  <li class="menu__item"
    :class="[currentPage === itemData.title ? itemData.class : '']"
  >
    <component :is="itemData.icon"/>
    {{ itemData.title }}
  </li>

</template>

<script lang="ts">

export default {
  name: 'CrmMenuItem',
  components: {
    DeskIcon: require('!vue-svg-loader!@/assets/img/menu/desk.svg'),
    AdministrationIcon: require('!vue-svg-loader!@/assets/img/menu/admin.svg'),
    PersonnelAccountingIcon: require('!vue-svg-loader!@/assets/img/menu/pad.svg'),
    RecruitmentIcon: require('!vue-svg-loader!@/assets/img/menu/staff.svg'),
    BotConstructorIcon: require('!vue-svg-loader!@/assets/img/menu/constructor.svg'),
    OnlineStoreIcon: require('!vue-svg-loader!@/assets/img/menu/market.svg'),
    PaymentsIcon: require('!vue-svg-loader!@/assets/img/menu/pay.svg'),
    CommunicationIcon: require('!vue-svg-loader!@/assets/img/menu/chat.svg'),
    ParsersBotsIcon: require('!vue-svg-loader!@/assets/img/menu/idea.svg'),
    AnalyticsIcon: require('!vue-svg-loader!@/assets/img/menu/analytics.svg'),
    MyOfficeIcon: require('!vue-svg-loader!@/assets/img/menu/user.svg'),
  },
  props: {
    currentPage: String,
    itemData: {
      id: Number,
      icon: String,
      title: String,
      path: String,
      class: String,
    },
  }
}

</script>

<style lang="scss">

  .menu__item {
    display: flex;
    align-items: center;
    padding: 12px 30px;
    cursor: pointer;
    background-color: transparent;
  }

  .menu__item svg {
    padding-right: 30px;
  }

  // ====================== Стили активных пунктов меню =========================

  .item__desk, .item__admin, .item__personnel, .item__recruitment,
  .item__constructor, .item__store, .item__payments,
  .item__communicate, .item__parsers, .item__analytics, .item__office {
    color: #FFFFFF;
  }

  li[class*="item__desk"] > svg,
  li[class*="item__admin"] > svg,
  li[class*="item__personnel"] > svg,
  li[class*="item__recruitment"] > svg,
  li[class*="item__constructor"] > svg,
  li[class*="item__store"] > svg,
  li[class*="item__payments"] > svg,
  li[class*="item__communicate"] > svg,
  li[class*="item__parsers"] > svg,
  li[class*="item__analytics"] > svg,
  li[class*="item__office"] > svg {
    color: #FFFFFF;
  }

  .item__desk {
    background-color: #2274A5;

  }

  .item__admin {
    background-color: #1E892F;
  }

  .item__personnel {
    background-color: #741E89;
  }

  .item__recruitment {
    background-color: #891E4B;
  }
  .item__constructor {
    background-color: #CF9603;
  }
  .item__store {
    background-color: #FF5C5C;
  }
  .item__payments {
    background-color: #1e7589;
  }
  .item__communicate {
    background-color: #321e89;
  }
  .item__parsers {
    background-color: #897b1e;
  }
  .item__analytics {
    background-color: #891e64;
  }
  .item__office {
    background-color: #ff6a00;
  }

  </style>
