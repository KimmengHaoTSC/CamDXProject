<template>
    <v-card class="rounded-0 pa-5" light>
        <v-container>
            <v-row >
                <v-col cols="12">
                    <div class="text-h3 bold font-weight-medium text-center">
                        {{ $t('homePage.contact.title') }}
                    </div>
                </v-col>
                <v-col cols="12">
                    <div class="text-md subtitle md-2 text-center">
                        {{ $t('homePage.contact.subtitle') }}
                    </div>
                </v-col>
            </v-row>
            <v-col>
                <v-row >
                    <v-col v-for="(item, index) in items" :key="index" cols="12" md="6" sm="12">
                        <div data-aos="zoom-in-up" data-aos-duration="1000">
                            <v-card class="greybackground" height="300px">
                                <v-card-title>
                                    <v-img 
                                        :contain="true" height="100" :src="require('assets/' + item.icon + '.png')"
                                        width="100"></v-img>
                                </v-card-title>
                                <v-card-text class="text-h5 font-weight-bold text-center">
                                    {{ $t(item.title) }}
                                </v-card-text>
                                <!-- eslint-disable vue/no-v-html -->
                                <v-card-text class="text-md text-center" v-html='$t(item.meaning)'>
                                <!-- eslint-disable vue/no-v-html -->
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
                meaning: 'homePage.contact.subdetail2',
            },
            {
                icon: 'contact3',
                title: 'homePage.contact.detail3',
                meaning: 'homePage.contact.subdetail3',
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
</style>