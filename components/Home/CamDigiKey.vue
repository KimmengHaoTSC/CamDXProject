<template>
    <v-card class="rounded-0 pa-5 backgroundTheme" dark>
        <v-container>
            <v-row>
                <v-col cols="12">
                    <div class="titleSize">
                        {{ $t('homePage.camdigikey.title') }}
                    </div>
                </v-col>
                <v-col cols="12">
                    <div class="subtitleSize md-2">
                        {{ $t('homePage.camdigikey.subtitle') }}
                    </div>
                </v-col>
            </v-row>
            <v-row>
                <v-col cols="12" md="4" sm="6" xs="12" class="d-flex align-center mb-6">
                    <v-card color="#C5C5C4" dark class="mr-15" width="400" height="200"></v-card>
                </v-col>
                <v-col col="12" md="8" sm="6" xs="12">
                    <v-row>
                        <v-col cols="12">
                            <div class="subtitleSize mb-4 text-justify">
                                {{ $t('homePage.camdigikey.content') }}
                            </div>
                        </v-col>
                        <v-col cols="12" md="4" sm="12" xs="12">
                            <v-btn 
                                width="100%"
                                :class="[(hoverAndroid ? 'foo-hover-true' : 'foo-hover-false') + ' text-capitalize']"
                                @mouseover="hoverAndroid = true" @mouseleave="hoverAndroid = false" >
                                <v-icon class="mr-4">mdi-google-play</v-icon>
                                Android
                            </v-btn>
                        </v-col>
                        <v-col cols="12" md="4" sm="12" xs="12">
                            <v-btn 
                                :class="[(hoverApple ? 'foo-hover-true' : 'foo-hover-false') + ' text-capitalize']"
                                width="100%" @mouseover="hoverApple = true" @mouseleave="hoverApple = false" >
                                <v-icon class="mr-4">mdi-apple</v-icon>
                                iOS
                            </v-btn>
                        </v-col>
                        <v-col cols="12" md="4" sm="12" xs="12">
                            <v-btn 
                                light width="100%" outlined
                                :class="[(hovered ? 'foo-hover-false' : 'foo-hover-true') + ' text-capitalize']"
                                @mouseover="hovered = true" @mouseleave="hovered = false">
                                Learn More
                                <v-icon class="ml-4">mdi-arrow-right</v-icon>
                            </v-btn>
                        </v-col>
                    </v-row>
                </v-col>
            </v-row>
        </v-container>
    </v-card>
</template>
<script>
export default {
    name: 'CamDigiKeypage',
    data: () => ({
        hovered: false,
        hoverAndroid: false,
        hoverApple: false,
    }),
}
</script>
<style>
.foo-hover-true {
    background: rgb(240, 240, 240) !important;
    color: rgb(59, 62, 123) !important;
}

.foo-hover-false {
    background: rgb(59, 62, 123) !important;
    color: rgb(255, 255, 255) !important;
}
</style>