<template>
    <v-card class="pa-5 backgroundTheme" dark>
        <v-container>
            <v-row justify="center">
                <v-col cols="6">
                    <v-row>
                    <v-col cols="12" md="6" xs="12"  align="center">
                    <v-btn  
                        depressed filled width="100%" href='https://play.google.com/store/apps/details?id=kh.gov.camdx.camdigikey' target="_blank"
                        :class="[(hoverAndroid ? 'foo-hover-true' : 'foo-hover-false') + ' mr-1 text-capitalize']"
                        @mouseover="hoverAndroid = true" @mouseleave="hoverAndroid = false">
                        <v-icon class="mr-4">mdi-google-play</v-icon>
                        Android
                    </v-btn>
                </v-col>
                    <v-col cols="12" md="6" xs="12"  align="center">
                    <v-btn  
                        depressed filled width="100%"  href='https://apps.apple.com/kh/app/camdigikey/id1509386989' target="_blank"
                        :class="[(hoverApple ? 'foo-hover-true' : 'foo-hover-false') + ' mr-1 text-none']"
                        @mouseover="hoverApple = true" @mouseleave="hoverApple = false">
                        <v-icon class="mr-4">mdi-apple</v-icon>
                        iOS
                    </v-btn>
                </v-col></v-row>
            </v-col>
            </v-row>

            <v-row>
                <v-col cols="12">
                    <div class="md-2 textSize text-center">
                        {{ $t('obrPage.devguide') }}
                    </div>
                </v-col>
            </v-row>

            <v-row cols="12">
                <v-col v-for="(item, index) in buttonItem" :key="index" cols="12" md="3" sm="6" xs="12" align="center" class="text-center">
                    <v-btn 
                        depressed  width="100%" :href='item.link' target="_blank" outlined
                        :class="[(item.variable ? 'text-hover-true' : 'text-hover-false') + ' mr-1 text-none']"
                        @mouseover="item.variable = false" @mouseleave="item.variable = true">
                    <v-icon class="mr-4">{{item.icon}}</v-icon>
                       {{item.label}}
                    </v-btn>
                </v-col>
            </v-row>
        </v-container>
    </v-card>
</template>
<script>
export default {
    name: 'GuidePage',
    data: () => ({
        hoverAndroid: false,
        hoverApple: false,
        hover1: false,
        hover2: false,
        hover3: false,
        hover4: false,
        buttonItem: [
            {
                icon: 'mdi-file-document',
                label: 'Documentation',
                link: "https://github.com/Techo-Startup-Center/CamDigiKey-Integration",
                variable : 'hover1'
            },
            {
                icon: 'mdi-google-play',
                label: 'Android',
                link: "https://github.com/Techo-Startup-Center/CamDigiKey-Sample-Code-Android",
                variable : 'hover2'
            },
            {
                icon: 'mdi-apple',
                label: ' iOS',
                link: "https://github.com/Techo-Startup-Center/CamDigiKey-Sample-Code-IOS",
                variable : 'hover3'
            },
            {
                icon: 'mdi-open-in-new',
                label: 'Web',
                link: "https://github.com/Techo-Startup-Center/CamDigiKey-Sample-Code-Server",
                variable : 'hover4'
            }
        ]
    }),
}
</script>
<style>
.white-button {
    background-color: white;
}

.foo-hover-true {
    background: rgb(255, 255, 255) !important;
    color: rgb(25, 118, 220) !important;
}

.foo-hover-false {
    background: rgb(25, 118, 220) !important;
    color: rgb(255, 255, 255) !important;
}

.text-hover-true {
    background: rgb(255, 255, 255) !important;
    color: rgb(21, 21, 22) !important;
}

.text-hover-false {
    background: rgb(30, 30, 30) !important;
    color:rgb(255, 255, 255) !important;
}
</style>