<template>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">
        <%= name %>
      </h1>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          rel="noopener noreferrer"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          rel="noopener noreferrer"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
    </div>
  </div>
</template>

<%_ if (typescript) { _%>
<script lang="ts">
<%_ } else { _%>
<script>
<%_ } _%>
<%_ if (composition) { _%>
import { defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({})
</script>
<%_ } else if (typescript) { _%>
import Vue from 'vue'

export default Vue.extend({})
</script>
<%_ } else { _%>
<script>
export default {}
</script>
<%_ } _%>

<style>
<%_ if (ui === 'tailwind') { _%>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
<%_ }
_%>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
