<template>
    <v-card class="rounded-0 pa-5 greybackground" light>
        <v-container>
            <v-col cols="12">
                <v-row class="pb-5">
                    <v-col cols="12">
                        <div class="titleSize">
                            {{ $t('homePage.servicerun.title') }}
                        </div>
                    </v-col>
                </v-row>
                <v-col>
                    <v-row align="center">
                        <v-col v-for="(item, index) in items" :key="index" cols="12" md="4" sm="12">
                            <v-card class="mx-auto justify-center " light>
                                <v-card color="primary" class="rounded-lg" height="200" dark>
                                    <v-card-title>
                                    </v-card-title>
                                    <v-card-text class="subtitleSize font-weight-bold text-left" color="white">
                                        {{ $t(item.title) }}
                                    </v-card-text>
                                </v-card>
                                <v-card-text class="textSize">
                                    {{ $t(item.meaning) }}
                                </v-card-text>
                                <v-card-actions class="justify-end">
                                    <v-btn
                                        text
                                        class="textSize text-capitalize" 
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
.box {
    box-shadow: none;
}
</style>