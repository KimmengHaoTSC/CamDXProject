<template>
    <v-card class="pa-md-10 backgroundTheme" dark>
        <v-container>
            <v-row class="ma-4 titleSize"> CamDX </v-row>
            <v-col cols="12">
                <v-row class="ma-4 textSize">
                    <v-col cols="12" md="5" sm="6" xs="12" >
                        <v-row class="mb-3">Ministry of Economy and Finance<br />
                            Phnom Penh, Cambodia
                        </v-row>
                        <v-row>Phone: (855) 81 888 296<br/>
                            Email: camdx@mef.gov.kh</v-row>
                    </v-col>
                    <v-col v-if="$route.path === '/' || $route.path == '/kh'" cols="12" md="3" sm="6" xs="12">
                        <v-row class="mb-5">
                            <v-icon>mdi-chevron-right</v-icon> 
                            <a @click="$vuetify.goTo('#overview')">
                                CamDX
                            </a>
                        </v-row>
                        <v-row class="mb-5">
                            <v-icon>mdi-chevron-right</v-icon> 
                            <a @click="$vuetify.goTo('#principles')">
                                Principles
                            </a>
                        </v-row>
                        <v-row class="mb-5">
                            <v-icon>mdi-chevron-right</v-icon> 
                            <a @click="$vuetify.goTo('#camdigikey')">
                                CamDigiKey
                            </a>
                        </v-row>
                    </v-col>
                    <v-col v-if="$route.path === '/' || $route.path == '/kh'" cols="12" md="2" sm="6" xs="12">
                        <v-row class="mb-5">
                            <v-icon>mdi-chevron-right</v-icon> 
                            <a @click="$vuetify.goTo('#service')">
                                Services
                            </a>
                        </v-row>
                        <v-row class="mb-5">
                            <v-icon>mdi-chevron-right</v-icon> 
                            <a @click="$vuetify.goTo('#faq')">
                                F.A.Q
                            </a>
                        </v-row>
                        <v-row class="mb-5">
                            <v-icon>mdi-chevron-right</v-icon> 
                            <a @click="$vuetify.goTo('#contact')">
                                Contact Us
                            </a>
                        </v-row>
                    </v-col>
                    <v-col cols="12" md="2" sm="6" xs="12" align="center">
                        <v-row  class="mb-5">Stay Connected</v-row>
                        <v-row>
                            <v-icon color="blue" large>mdi-facebook</v-icon>
                        </v-row>
                    </v-col>
                </v-row>
            </v-col>
            <v-divider></v-divider>
            <v-row class="ma-4" >
                <v-col cols="12" md="6" sm="12" xs="12">
                    <div class="textSize">©2020-2022 CamDX. All Rights Reserved</div>
                </v-col>
                <v-col cols="12" md="6" sm="12" xs="12" align="right" >
                    <div class="textSize">Terms of Use | Privacy Policy</div>

                </v-col>
            </v-row>
        </v-container>
    </v-card>
</template>

<script>
export default {
    name: 'FooterMyPage'
}
</script>

<style>
a {
    color: white !important;
}
</style>