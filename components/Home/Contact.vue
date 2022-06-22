<template>
    <v-card class="rounded-0 pa-5" light>
        <v-container>
            <v-row >
                <v-col cols="12">
                    <div class="titleSize">
                        {{ $t('homePage.contact.title') }}
                    </div>
                </v-col>
                <v-col cols="12">
                    <div class="subtitleSize md-2">
                        {{ $t('homePage.contact.subtitle') }}
                    </div>
                </v-col>
            </v-row>
            <v-col>
                <v-row >
                    <v-col v-for="(item, index) in items" :key="index" cols="12" md="6" sm="12">
                        <div data-aos="zoom-in-up" data-aos-duration="700">
                            <v-card class="greybackground" height="350px">
                                <v-card-title>
                                    <v-img 
                                        :contain="true" height="100" :src="require('assets/' + item.icon + '.png')"
                                        width="100"></v-img>
                                </v-card-title>
                                <v-card-text class="subtitleSize font-weight-bold">
                                    {{ $t(item.title) }}
                                </v-card-text>
                                <!-- eslint-disable vue/no-v-html -->
                                <v-card-text class="textSize text-center" v-html='$t(item.meaning)'>
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
                title: 'homePage.contact.detail1',
                meaning: 'homePage.contact.subdetail1',
            },
            {
                icon: 'contact2',
                title: 'homePage.contact.detail2',
                meaning: "<a href=\"tel:(855) 81 888 296\" > (855) 81 888 296 </a>",
            },
            {
                icon: 'contact3',
                title: 'homePage.contact.detail3',
                meaning: "<a href=\"mailto:camdx@mef.gov.kh\" > camdx@mef.gov.kh </a><br><br><a href=\"mailto:camdx@mef.gov.kh\" > registrationservices@mef.gov.kh </a>",
            },
            {
                icon: 'contact3',
                title: 'homePage.contact.detail4',
                meaning: 'homePage.contact.subdetail4',
            },
        ]
    }),
}
</script>
<style>
    a {
        color: primary !important;
        text-decoration: none
    }
</style>