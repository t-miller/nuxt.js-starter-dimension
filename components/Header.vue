<template>
  <header id="header">
    <div class="logo">
      <font-awesome-icon :icon="faGem" transform="grow-18" />
    </div>
    <div class="content">
      <div class="inner">
        <h1>Dimension</h1>
        <p>
          A fully responsive site template designed by
          <a href="https://html5up.net">HTML5 UP</a> and released
          <br />
          for free under the
          <a href="https://html5up.net/license">Creative Commons</a> license.
        </p>
      </div>
    </div>
    <nav>
      <ul>
        <li v-for="link in links" :key="link.index">
          <a href="javascript:;" @click="$emit('open-article', link.label)">{{
            link.label
          }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
import { faGem } from '@fortawesome/fontawesome-free-regular'
export default {
  data() {
    return {
      links: [
        { label: 'intro' },
        { label: 'work' },
        { label: 'about' },
        { label: 'contact' },
      ],
    }
  },
  computed: {
    faGem() {
      return faGem
    },
  },
}
</script>
