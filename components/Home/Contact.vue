<template>
    <v-card class="rounded-0 pa-10" light>
        <v-container>
            <v-row >
                <v-col cols="12">
                    <div class="text-h3 bold font-weight-medium text-center">
                        Contact Us
                    </div>
                </v-col>
                <v-col cols="12">
                    <div class="text-md subtitle md-2 text-center">
                        We are happy to discuss with you whether you want to find more information or you want to join
                        CamDX.
                    </div>
                </v-col>
            </v-row>
            <v-col>
                <v-row >
                    <v-col v-for="(item, index) in items" :key="index" cols="12" md="6" sm="12">
                        <div data-aos="zoom-in-up" data-aos-duration="2500">
                            <v-card color="#F8F9FA" height="300px">
                                <v-card-title>
                                    <v-img 
                                        :contain="true" height="100" :src="require('assets/' + item.icon + '.png')"
                                        width="100"></v-img>
                                </v-card-title>
                                <v-card-text class="text-h5 font-weight-bold text-center">
                                    {{ item.title }}
                                </v-card-text>
                                <v-card-text class="text-md text-center" v-text="item.meaning">
                                    <!-- {{  }} -->
                                </v-card-text>
                            </v-card>
                        </div>
                    </v-col>
                </v-row>
            </v-col>
        </v-container>
    </v-card>
</template>
<script>
export default {
    name: 'FAQpage',
    data: () => ({
        items: [
            {
                icon: 'contact1',
                title: 'ADDRESS',
                meaning: 'Ministry of Economy and Finance St.92, Wat Phnom, Daun Penh, Phnom Penh, Cambodia',
            },
            {
                icon: 'contact2',
                title: 'CALL US',
                meaning: '(855) 81 888 296',
            },
            {
                icon: 'contact3',
                title: 'EMAIL US',
                meaning: 'camdx@mef.gov.kh\nregistrationservices@mef.gov.kh',
            },
            {
                icon: 'contact3',
                title: 'WORKING US',
                meaning: 'Mon - Fri: 8AM to 5PM<br/>Except Public Holidays',
            },
        ]
    }),
}
</script>
<style>
</style>