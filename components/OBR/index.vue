<template>
        <v-card class="rounded-0 pa-10" light>
            <v-container>
                <v-col cols="12">
                    <div class="text-h3 bold font-weight-medium">
                        CamDigiKey, {{$t('camAuthenApp')}}
                    </div>
                </v-col>
                <v-col cols="12">
                    <div class="text-md">
                        CamDigiKey is a secure yet easy mobile application to authenticate oneself digitally to access to
                        various government digital services running through CamDX. Users must register to obtain valid
                        digital identity. To login, users simply use the application to scan the QR code appeared in the
                        login screen of the government portals. Online Business Registration is the first government portal
                        that uses CamDigiKey to authenticate the user digital identity.
                    </div>
                </v-col>
                <v-card color="#C5C5C4" light height="300"></v-card>

                <v-col cols="12" class="pa-15">
                    <v-row>
                        <div class="text-h3 font-weight-medium text-center">
                            New Features
                        </div>
                    </v-row>
                    <v-row>
                        <v-col v-for="(item, index) in items" :key="index" data-aos="fade-left" cols="12" md="3" sm="6" xs="6">
                                <v-card-title>
                                    <v-img 
                                        :contain="true" height="100"
                                        :src="require('assets/partner' + (index + 1) + '.png')" width="100"></v-img>
                                </v-card-title>
                                <v-card-text class="text-h5 font-weight-bold text-center">
                                    {{ item.title }}
                                </v-card-text>
                        </v-col>
                    </v-row>
                </v-col>
            </v-container>
        </v-card>
</template>

<script>
export default {
    name: 'OBRindex',
    data: () => ({
        items: [
            {
                icon: 'feature1',
                title: 'Liveness face detection',
            },
            {
                icon: 'feature2',
                title: 'Machine readable zone (MRZ) code reading',
            },
            {
                icon: 'feature3',
                title: 'App-to-app integration',
            },
            {
                icon: 'feature3',
                title: 'Web-to-web integration',
            },
        ]
    })
}
</script>

<style>
</style>