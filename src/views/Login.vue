<template>
  <div class="login">
      <h1>Login</h1>
      <section>
        <button @click="login">login</button>
      </section>
  </div>
</template>

<script lang="ts">
import { Vue } from "vue-property-decorator";
// import * as netlifyIdentity from "netlify-identity-widget";
const netlifyIdentity = require('netlify-identity-widget');

// export default class Login extends Vue {
//   mounted() {
//     console.log("init");
//     netlifyIdentity.init()
//   }
//   async login() {
//     console.log("login");
//     netlifyIdentity.open()
//   }
// }
export default Vue.extend({
  methods: {
    async login() {
      console.log("login");
      netlifyIdentity.open()
    }
  },
  mounted() {
    console.log("init");
    netlifyIdentity.init()
  },
})
</script>
 