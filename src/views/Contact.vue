<template>
  <div class="contact">
    <h2 class="mt-3">Contact</h2>
    <div class="pt-3 mb-5">
      <span class="h2 mt-3">Uitlaatservice</span><br />
      <span class="h2"><strong><q>De Zesvoeter</q></strong></span><br />
      <span class="h5">(Zeist en omstreken)</span><br /><br />
      <span class="h4"><router-link class="" to="/over-mij">Aukje Wind</router-link></span><br />
      <br />
      <a href="https://wa.me/31648077493" class="btn btn-md btn-success">
        Contact via <i class="fab fa-whatsapp"></i> WhatsApp
      </a>
      <br />
      <a id="mail" class="mt-2 btn btn-md btn-primary" v-if="dmail">
        Contact per <i class="far fa-envelope"></i> e-mail
      </a>
      <Vol />
    </div>
    <p class="mt-3 mb-5">
      KvK nummer: <b><a href="https://www.kvk.nl/zoeken/?source=all&q=76850994&start=0&site=kvk2014" target="_blank">76850994</a></b>
    </p>
  </div>
</template>

<script>
import Vol from './partials/Vol'

export default {
  name: 'contact',
  components: {
    Vol
  },
  data () {
    return {
      dmail: true
    }
  },
  mounted () {
    document.querySelector('#mail').setAttribute('href', 'mailto:aukje' + '@' + 'wind.cd')
  }
}
</script>

<style lang="scss" scoped>
</style>
