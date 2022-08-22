<template>
  <app-header> </app-header>
  <app-hero> </app-hero>
  <app-advantages> </app-advantages>
  <app-service> </app-service>
  <app-tariff> </app-tariff>
  <app-test> </app-test>
</template>

<script>
import AppHeader from "../components/invoiceLandingPage/AppHeader.vue";
import AppHero from "../components/invoiceLandingPage/AppHero.vue";
import AppAdvantages from "../components/invoiceLandingPage/AppAdvantages.vue";
import AppService from "../components/invoiceLandingPage/AppService.vue";
import AppTest from "../components/invoiceLandingPage/testbtn.vue";
import AppTariff from "../components/invoiceLandingPage/AppTariff.vue";
export default {
  components: {
    AppHeader,
    AppHero,
    AppAdvantages,
    AppService,
    AppTest,
    AppTariff,
  },
};
</script>

<style></style>
