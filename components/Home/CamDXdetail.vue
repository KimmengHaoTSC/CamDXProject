<template>

    <!-- <section id="title"> -->
    <v-card light class="rounded-0 pa-5" outlined>
        <v-container>
            <v-row class="d-flex align-center mb-6">
                <v-col cols="12" md="6" sm="12" xs="12">
                    <v-row>
                        <div class="titleSize bold mb-4">
                            {{ $t('homePage.camdxDetail.whatisCamDX') }}
                        </div>
                        <div class="subtitleSize mb-4 text-justify">
                            {{ $t('homePage.camdxDetail.isCamDX') }}
                        </div>
                    </v-row>
                </v-col>
                <v-col cols="12" md="6" sm="12" xs="12" >
                        <v-img 
                            data-aos="fade-up" data-aos-duration="450"
                            :src="require('@/assets/camdx.png')" class="img-fluid"></v-img>
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