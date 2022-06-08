<template>
    <v-card class="rounded-0 pa-10" dark color="#16184E">
        <v-container>
            <v-row>
                <v-col cols="12">
                    <div class="text-h3 bold font-weight-medium text-center">
                        CamDigiKey, a Mobile Authentication Application
                    </div>
                </v-col>
                <v-col cols="12">
                    <div class="text-md subtitle md-2 text-center">
                        A secure yet easy mobile application to authenticate oneself digitally to access to various
                        government digital services running through CamDX.
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
                            <div class="text-h6 mb-4">
                                Users must register to obtain valid digital identity. To login, users simply use the
                                application
                                to scan the QR code appeared in the login screen of the government portals. Online
                                Business
                                Registration is the first government portal that uses CamDigiKey to authenticate the
                                user
                                digital identity.
                            </div>
                        </v-col>
                        <v-col cols="12" md="4" sm="12" xs="12">
                            <v-btn width="100%"
                                :class="[(hoverAndroid ? 'foo-hover-true' : 'foo-hover-false') + ' text-capitalize']"
                                @mouseover="hoverAndroid = true" @mouseleave="hoverAndroid = false">
                                <v-icon class="mr-4">mdi-google-play</v-icon>
                                Android
                            </v-btn>
                        </v-col>
                        <v-col cols="12" md="4" sm="12" xs="12">
                            <v-btn :class="[(hoverApple ? 'foo-hover-true' : 'foo-hover-false') + ' text-capitalize']"
                                width="100%" @mouseover="hoverApple = true" @mouseleave="hoverApple = false">
                                <v-icon class="mr-4">mdi-apple</v-icon>
                                iOS
                            </v-btn>
                        </v-col>
                        <v-col cols="12" md="4" sm="12" xs="12">
                            <v-btn light width="100%" outlined
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
        buttonItem: [
            {
                icon: '',
                bgcolor: 'primary',
                label: 'Android',
                link: ''
            },
            {
                icon: '',
                bgcolor: 'primary',
                label: 'iOS',
                link: ''
            },
            {
                icon: '',
                bgcolor: 'white',
                label: 'Learn more',
                link: ''
            }
        ]
    }),
}
</script>
<style>
.foo-hover-true {
    background: rgb(255, 255, 255) !important;
    color: rgb(25, 118, 220) !important;
}

.foo-hover-false {
    background: rgb(25, 118, 220) !important;
    color: rgb(255, 255, 255) !important;
}
</style>