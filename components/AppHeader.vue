<template>
  <div class="app-container container mx-auto">
    <div class="app-header py-10 flex justify-between items-center">
      <app-logo class="app-header__logo" />
      <app-header-navigation />
    </div>
  </div>
</template>

<script>
  import AppLogo from './base/AppLogo'
  import AppHeaderNavigation from './AppHeaderNavigation'

  export default {
    components: {
      AppLogo,
      AppHeaderNavigation,
    }
  }
</script>