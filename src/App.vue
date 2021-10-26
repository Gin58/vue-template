<template>
  <div class="test">
    <h1 class="test__test">
      Vue Samle {{ getters.getCount() }}
    </h1>
    <CoverComponent />
    <button @click="actions.increment()">
      ぷらす
    </button>
    <button @click="actions.decrement()">
      まいなす
    </button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import CoverComponent from './components/CoverComponent.vue'
import { useStore } from './store'

export default defineComponent({
  components: {
    CoverComponent,
  },

  setup() {
    const {
      state,
      actions,
      getters,
    } = useStore().useStoreTop
    return {
      state,
      actions,
      getters,
    }
  },
})
</script>

<style lang="scss" scoped>
.test {
  &__test {
    color: red;
  }
}
</style>
