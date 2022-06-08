<template>
    <section id="home">
        <MainTitle></MainTitle>
        <!-- <section id="tab"> -->
        <section id="overview">
            <Tab :tabbgcolor="'#FFFFFF'"></Tab>
        <!-- </section> -->

        <!-- <v-btn class="ma-2" color="secondary" @click="expand2 = !expand2">
            Expand X Transition
        </v-btn> -->

            <CamDXdetail></CamDXdetail>
            <MainGoal></MainGoal>
        </section>

        <section id="principles">
            <DesignProperty></DesignProperty>

        </section>
        <section id="camdigikey">
            <MainComponent></MainComponent>
        </section>
        <section id="service">
            <SecureServer></SecureServer>
            <ExchangeData></ExchangeData>
            <CamDigiKey></CamDigiKey>
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
import Tab from '../components/Home/Tab.vue';
import CamDXdetail from '../components/Home/CamDXdetail.vue';
import DesignProperty from '../components/Home/DesignProperty.vue';
import MainComponent from '../components/Home/MainComponent.vue';
import SecureServer from '../components/Home/SecureServer.vue';
import ExchangeData from '../components/Home/ExchangeData.vue';
import CamDigiKey from '../components/Home/CamDigiKey.vue';
import ServiceRun from '../components/Home/ServiceRun.vue';
import Partner from '../components/Home/Partner.vue';
import FAQ from '../components/Home/FAQ.vue';
import Contact from '../components/Home/Contact.vue';
import MainTitle from '../components/Home/MainTitle.vue';
export default {
    name: "IndexPage",
    components: { MainTitle, Tab, CamDXdetail, DesignProperty, MainComponent, SecureServer, ExchangeData, CamDigiKey, ServiceRun, Partner, FAQ, Contact },
    data: () => ({
        expand2: false,
    }),
}
</script>

<style>
</style>
