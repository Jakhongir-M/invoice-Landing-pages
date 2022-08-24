<template>
  <app-header> </app-header>
  <app-hero> </app-hero>
  <app-advantages> </app-advantages>
  <app-service> </app-service>
  <app-tariff> </app-tariff>
  <app-klients> </app-klients>
  <app-footers> </app-footers>
</template>

<script>
import AppHeader from "../components/invoiceLandingPage/AppHeader.vue";
import AppHero from "../components/invoiceLandingPage/AppHero.vue";
import AppAdvantages from "../components/invoiceLandingPage/AppAdvantages.vue";
import AppService from "../components/invoiceLandingPage/AppService.vue";
import AppFooters from "../components/invoiceLandingPage/AppFooters.vue";
import AppTariff from "../components/invoiceLandingPage/AppTariff.vue";
import AppKlients from "../components/invoiceLandingPage/AppKlients.vue";
export default {
  components: {
    AppHeader,
    AppHero,
    AppAdvantages,
    AppService,
    AppTariff,
    AppKlients,
    AppFooters,
  },
};
</script>

<style></style>
