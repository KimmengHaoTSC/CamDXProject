<template>
    <v-card class="pa-5" dark color="#16184E">
        <v-container>
            <v-col cols="12">
                    <div class="text-h3 font-weight-medium text-center pb-5">
                        Our Partners
                    </div>
                <v-row>
                    <v-col v-for="(item, index) in 5" :key="index" align="center"
                            data-aos="flip-right" data-aos-duration="1500">
                        <v-img :contain="true" height="100" :src="require('assets/partner' + item + '.png')" width="100">
                        </v-img>
                    </v-col>
                </v-row>
            </v-col>
        </v-container>
    </v-card>
</template>
<script>
export default {
    name: 'PartnerPage',
    data: () => ({
    }),
}
</script>
<style>
</style>