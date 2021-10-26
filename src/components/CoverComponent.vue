<template>
  <div class="test__test">
    test components
    <div class="test__test">
      test components
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({})
</script>

<style lang="scss" scoped>
.test {
  &__text {
    color: blue;
  }
}
</style>
