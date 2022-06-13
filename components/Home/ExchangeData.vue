<template>
    <v-card color="#F8F9FA" class="rounded-0 pa-10" light>
        <v-container>
            <v-row>
                <v-col cols="12">
                    <div class="text-h3 bold font-weight-medium text-center">
                        {{ $t('homePage.exchange.title') }}
                    </div>
                </v-col>
                <v-col cols="12">
                    <div class="text-md subtitle md-2 text-center">
                        {{ $t('homePage.exchange.subtitle') }}
                    </div>
                </v-col>
            </v-row>
            <v-col>
                <v-card-text>
                    <v-list-item three-line>
                        <v-row>
                            <v-col v-for="(item, index) in items" :key="index" cols="12" md="4" sm="12">
                                <div data-aos="zoom-in-up">
                                    <v-card-title>
                                        <v-img 
                                            :contain="true" height="100" :src="require('assets/' + item.icon + '.png')"
                                            width="100"></v-img>
                                    </v-card-title>
                                    <v-card-text class="text-h5 font-weight-bold text-center">
                                        {{ $t(item.title) }}
                                    </v-card-text>
                                    <v-card-text class="text-md text-center">
                                        {{ $t(item.meaning) }}
                                    </v-card-text>
                                    </div>
                            </v-col>
                        </v-row>
                    </v-list-item>
                </v-card-text>
            </v-col>
        </v-container>
    </v-card>
</template>
<script>
export default {
    name: 'ExchangeDatapage',
    data: () => ({
        items: [
            {
                icon: 'exchange1',
                title: 'homePage.exchange.confidentiality.title',
                meaning: 'homePage.exchange.confidentiality.meaning',
            },
            {
                icon: 'exchange2',
                title: 'homePage.exchange.availability.title',
                meaning: 'homePage.exchange.availability.meaning',
            },
            {
                icon: 'exchange3',
                title: 'homePage.exchange.integrity.title',
                meaning: 'homePage.exchange.integrity.meaning',
            },
        ]
    })
}
</script>
<style>
.topbelow {
    top: 50%;
    bottom: 50%
}

.font-title {

    font-family: 'Roboto';
    font-style: normal;
    font-weight: 700;
    font-size: 50px;
    line-height: 150%;
}

.subtitle {
    font-family: 'Roboto';
    font-style: normal;
    font-weight: 400;
    font-size: 24px;
    line-height: 150%;
    text-align: center;
}

.box {
    box-shadow: none;
}
</style>