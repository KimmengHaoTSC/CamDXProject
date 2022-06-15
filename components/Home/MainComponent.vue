<template>
    <v-card class="rounded-0 pa-5 greybackground" light>
        <v-container>
            <v-row>
                <v-col cols="12">
                    <div class="text-h3 font-weight-medium text-center">
                        {{ $t('homePage.components.title') }}
                    </div>
                </v-col>
                <v-col cols="12">
                    <div class="text-md subtitle md-2 text-center">
                        {{ $t('homePage.components.subtitle') }}
                    </div>
                </v-col>
            </v-row>
            <v-col>
                <v-card class="rounded-xl pa-md-5 backgroundTheme" dark >
                    <v-card-text v-for="(item, index) in items" :key="index">
                        <v-row>
                            <v-col cols="12" md="2" sm="2" xs="12">
                                <div data-aos="fade-right">
                                    <v-img 
                                        :src="require('assets/' + item.icon + '.png')" :contain="true"
                                        max-height="100px">
                                    </v-img>
                                </div>
                            </v-col>
                            <v-col cols="12" md="10" sm="10" xs="12">
                                <div>
                                    <div class="text-h6 mb-4 font-weight-medium">
                                        {{ $t(item.title) }}
                                    </div>
                                    <div class="text-md mb-4 text-justify">
                                        {{ $t(item.meaning) }}
                                    </div>
                                </div>
                            </v-col>
                        </v-row>
                    </v-card-text>
                </v-card>
            </v-col>
        </v-container>
    </v-card>
</template>
<script>
export default {
    name: 'MainComponentpage',
    data: () => ({
        items: [
            {
                icon: 'component1',
                title: 'homePage.components.core.title',
                meaning: 'homePage.components.core.meaning',
            },
            {
                icon: 'component2',
                title: 'homePage.components.trusted.title',
                meaning: 'homePage.components.trusted.meaning',
            },
            {
                icon: 'component3',
                title: 'homePage.components.members.title',
                meaning: 'homePage.components.members.meaning',
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
</style>