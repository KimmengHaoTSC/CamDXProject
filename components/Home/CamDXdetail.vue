<template>

    <!-- <section id="title"> -->
    <v-card light class="rounded-0 pa-10" outlined>
        <v-container>
            <v-row>
                <v-col cols="12" md="6" class="d-flex align-center mb-6" align="center">
                    <v-row>
                        <div class="text-h3 bold mb-4 font-weight-medium">
                            What is CamDX?
                        </div>
                        <div class="text-h6 mb-4 text-justify">

                            CamDX stands for Cambodia Data eXchange, which adopts the model of X-Road of
                            Estonia. CamDX
                            is a
                            unified yet decentralized data exchange layer between information systems that
                            offers a
                            standardized and secure way to provide and consume services. CamDX ensures
                            confidentiality,
                            integrity, and interoperability between a multitude of different data exchange
                            parties.
                        </div>
                    </v-row>
                </v-col>
                <v-col cols="12" md="6" sm="12" xs="12" align="center">
                    <div data-aos="fade-up" data-aos-duration="3000">
                        <v-img 
                            :src="require('@/assets/camdx.png')" :contain="true" height="400px"></v-img>
                    </div>
                </v-col>
            </v-row>
        </v-container>
    </v-card>
    <!-- </section> -->

</template>
<script>
export default {

}
</script>
<style>
.font-title {
    font-family: 'Roboto';
    font-style: normal;
    font-weight: 700;
    font-size: 60px;
    line-height: 150%;
}

.subtitle {

    font-family: 'Roboto';
    font-style: normal;
    font-weight: 400;
    font-size: 24px;
    line-height: 150%;
}

.topbelow {

    top: 50%;
    bottom: 50%
}
</style>