<template>

  <ul class="menu__list">

    <nuxt-link
      v-for="item in items"
      class="item__office"
      v-on:click="makeActive('item__office')"
      :to=item.path
    >
      <li class="menu__item">
        {{ item.icon }}
        {{ item.title }}
      </li>
    </nuxt-link>

  </ul>

</template>

<script lang="ts">
import DeskIcon from '@/assets/img/menu/desk.svg'
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
  data() {
    return {
      items: [
        {id: 1, title: 'Рабочий стол', icon: DeskIcon, path: '/desk'},
        {id: 2, title: 'Администрирование', icon: '<AdministrationIcon/>', path: '/admin'},
        {id: 3, title: 'Кадровый учет', icon: `<PersonnelAccountingIcon/>`, path: '/personnel'},
        {id: 4, title: 'Подбор персонала', icon: `<RecruitmentIcon/>`, path: '/recruitment'},
        {id: 5, title: 'Конструктор ботов', icon: `<BotConstructorIcon/>`, path: '/constructor'},
        {id: 6, title: 'Интернет-магазин', icon: `<OnlineStoreIcon/>`, path: '/store'},
        {id: 7, title: 'Оплаты', icon: `<PaymentsIcon/>`, path: '/payments'},
        {id: 8, title: 'Общение', icon: `<CommunicationIcon/>`, path: '/communication'},
        {id: 9, title: 'Парсеры и боты', icon: `<ParsersBotsIcon/>`, path: '/parsers'},
        {id: 10, title: 'Статистика', icon: `<AnalyticsIcon/>`, path: '/analytics'},
        {id: 11, title: 'Мой кабинет', icon: `<MyOfficeIcon/>`, path: '/office'},
      ]
    }

  },
  props: ['id', 'title', 'icon', 'path'],
}

</script>

<style lang="scss">

</style>
