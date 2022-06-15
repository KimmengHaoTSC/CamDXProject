<template>

    <!-- <section id="title"> -->
    <v-card light class="rounded-0 pa-5" outlined>
        <v-container>
            <v-row>
                <v-col cols="12" md="6" class="d-flex align-center mb-6" align="center">
                    <v-row>
                        <div class="titleSize bold mb-4">
                            {{ $t('homePage.camdxDetail.whatisCamDX') }}
                        </div>
                        <div class="subtitleSize mb-4 text-justify">
                            {{ $t('homePage.camdxDetail.isCamDX') }}
                        </div>
                    </v-row>
                </v-col>
                <v-col cols="12" md="6" sm="12" xs="12" align="center">
                    <div data-aos="fade-up" data-aos-duration="500">
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