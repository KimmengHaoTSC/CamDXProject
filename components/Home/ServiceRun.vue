<template>
    <v-card class="rounded-0 pa-5 greybackground" light>
        <v-container>
            <v-col cols="12">
                <v-row class="pb-5">
                    <v-col cols="12">
                        <div class="text-h3 bold font-weight-medium text-center">
                            {{ $t('homePage.servicerun.title') }}
                        </div>
                    </v-col>
                </v-row>
                <v-col>
                    <v-row align="center">
                        <v-col v-for="(item, index) in items" :key="index" cols="12" md="4" sm="12">
                            <v-card class="card-cus justify-center box pa-1" light height="400px">
                                <v-card color="primary" class="rounded-lg" height="200" dark>
                                    <v-card-title>
                                    </v-card-title>
                                    <v-card-text class="text-h5 font-weight-bold " color="white">
                                        {{ $t(item.title) }}
                                    </v-card-text>
                                </v-card>
                                <v-card-text class="text-md">
                                    {{ $t(item.meaning) }}
                                </v-card-text>
                                <v-card-actions class="float-right">
                                    <v-btn
                                        text
                                        class="text-capitalize"
                                    >
                                        {{ $t('homePage.servicerun.visitSite') }}
                                        <v-icon>mdi-arrow-right-thin</v-icon>
                                    </v-btn>
                                </v-card-actions>
                            </v-card>
                        </v-col>
                    </v-row>
                </v-col>
            </v-col>
        </v-container>
    </v-card>

</template>
<script>
export default {
    name: 'ServiceRunpage',
    data: () => ({
        items: [
            {
                image: 'service1',
                title: "homePage.servicerun.onlineBusiness.title",
                meaning: "homePage.servicerun.onlineBusiness.meaning",
            },
            {
                image: 'service2',
                title: "homePage.servicerun.globaltravel.title",
                meaning: "homePage.servicerun.globaltravel.meaning",
            },
            {
                image: 'service3',
                title: "homePage.servicerun.validation.title",
                meaning: "homePage.servicerun.validation.meaning",
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