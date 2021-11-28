<template>
  <div>
    <ul class="flex items-center">
      <li class="ml-10" v-for="nav in navigationList">
        <app-button
           v-if="nav.type === 'button'"
           :label="nav.label"
           rounded
        />

        <a v-else href="#">{{ nav.label }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
  import AppButton from './base/AppButton'

  export default {
    components: {
      AppButton
    },

    data() {
      return {
        navigationList: [
          {
            label: 'How it works',
            url: '#how-it-works',
          },
          {
            label: 'Pricing',
            url: '#pricing',
          },
          {
            label: 'Request Beta',
            type: 'button',
          }
        ]
      }
    }
  }
</script>