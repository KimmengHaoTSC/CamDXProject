<template>
  <section id="home">
    <MainTitle></MainTitle>
    <section id="overview">
      <Tab></Tab>
      <CamDXdetail></CamDXdetail>
      <MainGoal></MainGoal>
    </section>
    <section id="principles">
      <DesignPrinciples></DesignPrinciples>
      <MainComponent></MainComponent>
      <SecureServer></SecureServer>
      <ExchangeData></ExchangeData>
    </section>
    <section id="camdigikey">
      <CamDigiKey></CamDigiKey>
    </section>
    <section id="service">
      <ServiceRun></ServiceRun>
    </section>
    <Partner></Partner>
    <section id="faq">
      <FAQ></FAQ>
    </section>
    <section id="contact">
      <Contact></Contact>
    </section>
  </section>
</template>

<script>
import Tab from '../components/Home/Tab.vue'
import CamDXdetail from '../components/Home/CamDXdetail.vue'
import DesignPrinciples from '../components/Home/DesignPrinciples.vue'
import MainComponent from '../components/Home/MainComponent.vue'
import SecureServer from '../components/Home/SecureServer.vue'
import ExchangeData from '../components/Home/ExchangeData.vue'
import CamDigiKey from '../components/Home/CamDigiKey.vue'
import MainGoal from '../components/Home/MainGoal.vue'
import ServiceRun from '../components/Home/ServiceRun.vue'
import Partner from '../components/Home/Partner.vue'
import FAQ from '../components/Home/FAQ.vue'
import Contact from '../components/Home/Contact.vue'
import MainTitle from '../components/Home/MainTitle.vue'
export default {
  name: 'IndexPage',
  components: {
    MainTitle,
    Tab,
    CamDXdetail,
    DesignPrinciples,
    MainComponent,
    MainGoal,
    SecureServer,
    ExchangeData,
    CamDigiKey,
    ServiceRun,
    Partner,
    FAQ,
    Contact,
  }
}
</script>

<style>
</style>
