<template>
    <v-card class="rounded-0 pa-5" light>
        <v-container>
            <v-row>
                <v-col cols="12">
                    <div class="titleSize">
                        {{ $t('homePage.secureserver.title') }}
                    </div>
                </v-col>
                <v-col cols="12">
                    <div class="subtitleSize md-2">
                        {{ $t('homePage.secureserver.subtitle') }}
                    </div>
                </v-col>
            </v-row>
            <v-row class="d-flex align-center mb-6">
                <v-col cols="12" md="8" sm="12" xs="12" >
                    <v-row v-for="(item, index) in items" :key="index" data-aos="fade-right">
                        <v-col cols="2" md="1" sm="1" xs="1">
                            <v-img :src="require('assets/point.png')" :contain="true" width="30" height="30">
                            </v-img>
                        </v-col>
                        <v-col cols="10" md="11" sm="11" xs="11" class="textSize">
                            {{ $t(item) }}
                        </v-col>
                    </v-row>
                </v-col>
                <v-col cols="12" md="4" sm="12" xs="12" data-aos="fade-left">
                    <v-img :src="require('assets/secure.png')" :contain="true" height="400"></v-img>
                </v-col>
            </v-row>
        </v-container>
    </v-card>
</template>
<script>
export default {
    name: 'SecureServerpage',
    data: () => ({
        items: [
            "homePage.secureserver.char1",
            "homePage.secureserver.char2",
            "homePage.secureserver.char3",
            "homePage.secureserver.char4",
            "homePage.secureserver.char5"
        ]
    })
}
</script>