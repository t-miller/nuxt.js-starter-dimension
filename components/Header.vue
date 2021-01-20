<template>
  <header id="header">
    <div class="logo">
      <font-awesome-icon :icon="faGem" />
    </div>
  </header>
</template>

<script>
import { faGem } from '@fortawesome/fontawesome-free-regular'
export default {
  computed: {
    faGem() {
      return faGem
    },
  },
}
</script>
