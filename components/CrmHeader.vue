<template>

  <div class="header">

    <div class="header__content">

      <StafferLogo/>
      <div class="header__menu">

        <h2 class="header__title">
          {{ title }}
        </h2>
        <div class="header__user">

          <UserAvatar/>
          <p class="header__name_user">
            Иванова Татьяна Владимировна
          </p>
          <div class="header__icons">
            <div class="icons__container">
              <NotificationIcon/>
              <div class="icons__badge">2</div>
            </div>
            <ExitIcon/>
          </div>

        </div>

      </div>

    </div>

  </div>

</template>

<script lang="ts">

export default {
  name: 'CrmHeader',
  components: {
    StafferLogo: require('!vue-svg-loader!@/assets/img/ITStaffer.svg'),
    UserAvatar: require('!vue-svg-loader!@/assets/img/avatar.svg'),
    NotificationIcon: require('!vue-svg-loader!@/assets/img/bell.svg'),
    ExitIcon: require('!vue-svg-loader!@/assets/img/exit.svg')
  },
  props: ['title']
}

</script>

<style lang="scss">

  .header__content, .header__menu, .header__user {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .header__menu {
    padding: 12px 20px ;
    background: #FFFFFF;
    border: 1px solid #BCDFE7;
    border-radius: 10px;
  }

  .header__title {
    font-size: 22px;
  }

  .header__name_user {
    padding: 0 16px;
  }

  .header__icons {
    display: flex;
  }

  .header__icons > svg:last-child {
    padding-left: 15px;
  }

  .icons__container {
    position: relative;
  }

  .icons__badge {
    background: #FF5C5C;
    font-size: 12px;
    text-align: center;
    color: #FFFFFF;
    padding: 4px 7px;
    border-radius: 56px;
    position: absolute;
    top: -10px;
    right: -8px;
  }

</style>
