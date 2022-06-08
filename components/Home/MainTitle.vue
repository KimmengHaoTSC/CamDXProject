<template>
    <v-card color="#16184E" width="100%" class="rounded-0 pa-10">
        <v-container>
            <v-row>
                <v-col cols="12" md="6" class="d-flex align-center mb-6">
                    <v-row >
                        <div class="text-h3 bold mb-10">
                            {{$t('mainTitle')}}
                        </div>
                        <div class="text-h6">
                            Securely allow multi-lateral data exchange between different information
                            systems over the Internet.
                        </div>
                    </v-row>
                </v-col>
                <v-col cols="12" md="6" align="center">
                    <!-- <div data-aos="fade-zoom-in"
                        data-aos-easing="ease-in-back"
                        data-aos-delay="300"
                        data-aos-offset="0"> -->
                        <v-img 
                            :contain="true" :src="require('@/assets/maintitle.png')">
                        </v-img>
                    <!-- </div> -->
                </v-col>
            </v-row>
            <v-col cols="12" class="pt-15" align="center">
                <v-btn icon @click="$vuetify.goTo('#tab')">
                <v-icon large>mdi-mouse</v-icon>
                </v-btn>
            </v-col>
        </v-container>
    </v-card>
</template>
<script>
export default {
    name: 'MaintitlePage',
    data: () => ({
        items: true
    }),
    methods: {
        alignment() {
            return this.items ? 'center' : 'left'
        }
    }
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
</style>