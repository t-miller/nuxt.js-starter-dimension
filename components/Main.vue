<template>
  <div id="main">
    <article
      id="intro"
      :class="[
        article === 'intro' ? 'active' : '',
        articleTimeout ? 'timeout' : '',
      ]"
    >
      <h2 class="major">Intro</h2>
      <span class="image main">
        <img src="~/assets/images/intro.jpg" alt="" />
      </span>
      <p>
        Aenean ornare velit lacus, ac varius enim ullamcorper eu. Proin aliquam
        facilisis ante interdum congue. Integer mollis, nisl amet convallis,
        porttitor magna ullamcorper, amet egestas mauris. Ut magna finibus nisi
        nec lacinia. Nam maximus erat id euismod egestas. By the way, check out
        my <a href="#work">awesome work</a>.
      </p>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis dapibus
        rutrum facilisis. Class aptent taciti sociosqu ad litora torquent per
        conubia nostra, per inceptos himenaeos. Etiam tristique libero eu nibh
        porttitor fermentum. Nullam venenatis erat id vehicula viverra. Nunc
        ultrices eros ut ultricies condimentum. Mauris risus lacus, blandit sit
        amet venenatis non, bibendum vitae dolor. Nunc lorem mauris, fringilla
        in aliquam at, euismod in lectus. Pellentesque habitant morbi tristique
        senectus et netus et malesuada fames ac turpis egestas. In non lorem sit
        amet elit placerat maximus. Pellentesque aliquam maximus risus, vel sed
        vehicula.
      </p>
      <div class="close" @click="$emit('close-article')"></div>
    </article>
    <article
      id="work"
      :class="[
        article === 'work' ? 'active' : '',
        articleTimeout ? 'timeout' : '',
      ]"
    >
      <h2 class="major">Work</h2>
      <span class="image main">
        <img src="~/assets/images/work.jpg" alt="" />
      </span>
      <p>
        Adipiscing magna sed dolor elit. Praesent eleifend dignissim arcu, at
        eleifend sapien imperdiet ac. Aliquam erat volutpat. Praesent urna nisi,
        fringila lorem et vehicula lacinia quam. Integer sollicitudin mauris nec
        lorem luctus ultrices.
      </p>
      <p>
        Nullam et orci eu lorem consequat tincidunt vivamus et sagittis libero.
        Mauris aliquet magna magna sed nunc rhoncus pharetra. Pellentesque
        condimentum sem. In efficitur ligula tate urna. Maecenas laoreet massa
        vel lacinia pellentesque lorem ipsum dolor. Nullam et orci eu lorem
        consequat tincidunt. Vivamus et sagittis libero. Mauris aliquet magna
        magna sed nunc rhoncus amet feugiat tempus.
      </p>
      <div class="close" @click="$emit('close-article')"></div>
    </article>
    <article
      id="about"
      :class="[
        article === 'about' ? 'active' : '',
        articleTimeout ? 'timeout' : '',
      ]"
    >
      <h2 class="major">About</h2>
      <span class="image main">
        <img src="~/assets/images/about.jpg" alt="" />
      </span>
      <p>
        Lorem ipsum dolor sit amet, consectetur et adipiscing elit. Praesent
        eleifend dignissim arcu, at eleifend sapien imperdiet ac. Aliquam erat
        volutpat. Praesent urna nisi, fringila lorem et vehicula lacinia quam.
        Integer sollicitudin mauris nec lorem luctus ultrices. Aliquam libero et
        malesuada fames ac ante ipsum primis in faucibus. Cras viverra ligula
        sit amet ex mollis mattis lorem ipsum dolor sit amet.
      </p>
      <div class="close" @click="$emit('close-article')"></div>
    </article>
    <article
      id="contact"
      :class="[
        article === 'contact' ? 'active' : '',
        articleTimeout ? 'timeout' : '',
      ]"
    >
      <h2 class="major">Contact</h2>
      <form method="post" action="#">
        <div class="field half first">
          <label htmlFor="name">Name</label>
          <input id="name" type="text" name="name" />
        </div>
        <div class="field half">
          <label htmlFor="email">Email</label>
          <input id="email" type="text" name="email" />
        </div>
        <div class="field">
          <label htmlFor="message">Message</label>
          <textarea id="message" name="message" rows="4"></textarea>
        </div>
        <ul class="actions">
          <li>
            <input type="submit" value="Send Message" class="special" />
          </li>
          <li>
            <input type="reset" value="Reset" />
          </li>
        </ul>
      </form>
      <ul class="icons">
        <li>
          <a href="#">
            <font-awesome-icon :icon="faTwitter" />
          </a>
        </li>
        <li>
          <a href="#">
            <font-awesome-icon :icon="faFacebook" />
          </a>
        </li>
        <li>
          <a href="#">
            <font-awesome-icon :icon="faInstagram" />
          </a>
        </li>
        <li>
          <a href="#">
            <font-awesome-icon :icon="faGithub" />
          </a>
        </li>
      </ul>
      <div class="close" @click="$emit('close-article')"></div>
    </article>
  </div>
</template>

<script>
import {
  faTwitter,
  faFacebook,
  faInstagram,
  faGithub,
} from '@fortawesome/fontawesome-free-brands'
export default {
  props: {
    article: {
      type: String,
      default: '',
    },
    articleTimeout: Boolean,
  },
  computed: {
    faTwitter() {
      return faTwitter
    },
    faFacebook() {
      return faFacebook
    },
    faInstagram() {
      return faInstagram
    },
    faGithub() {
      return faGithub
    },
  },
}
</script>

<style scoped>
#main {
  display: flex;
}
article {
  display: none;
}
</style>
