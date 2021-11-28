<template>
  <div class="app-btn app-btn__default" :class="buttonClassNames">
    {{ label }}
  </div>
</template>

<script>
  export default {
    props: {
      label: {
        type: String,
      },

      rounded: {
        type: Boolean,
      },
    },

    computed: {
      buttonClassNames() {
        return {
          'app-btn__rounded': this.rounded
        }
      }
    },
  }
</script>

<style lang="scss">
  .app-btn {
    display: inline-flex;
    background-color: transparent;
    border: none;
    user-select: none;
    padding: 12px 32px;
    border-radius: 6px;
    font-weight: 400;

    &:hover {
      cursor: pointer;
   }
  }


  // Button types
  .app-btn {
    &__default {
      background-color: #000;
      color: #fff;
    }
  }

  // Button variants
  .app-btn {
    &__rounded {
      border-radius: 26px;
    }
  }
</style>