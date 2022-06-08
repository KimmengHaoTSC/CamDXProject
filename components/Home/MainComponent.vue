<template>
    <v-card color="#F8F9FA" class="rounded-0 pa-10" light>
        <v-container>
            <v-row>
                <v-col cols="12">
                    <div class="text-h3 font-weight-medium text-center">
                        CamDX Components
                    </div>
                </v-col>
                <v-col cols="12">
                    <div class="text-md subtitle md-2 text-center">
                        CamDX comprises three main components namely core components, trusted components and its
                        members.
                    </div>
                </v-col>
            </v-row>
            <v-col>
                <v-card color="#16184E" dark class="rounded-xl pa-md-5">
                    <v-card-text v-for="(item, index) in items" :key="index">
                        <v-row>
                            <v-col cols="12" md="2" sm="2" xs="12">
                                <div data-aos="fade-right">
                                    <v-img :src="require('assets/' + item.icon + '.png')" :contain="true"
                                        max-height="100px">
                                    </v-img>
                                </div>
                            </v-col>
                            <v-col cols="12" md="10" sm="10" xs="12">
                                <div>
                                    <div class="text-h6 mb-4 font-weight-medium">
                                        {{ item.title }}
                                    </div>
                                    <div class="text-md mb-4 text-justify">
                                        {{ item.meaning }}
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
                title: 'Core components',
                meaning: 'CamDX is a distributed system with no central database performing only data exchange.',
            },
            {
                icon: 'component2',
                title: 'Trusted components',
                meaning: 'Enterprise-class security at the application level by ensuring the authenticity, integrity and non-repudiation of the exchanged data.',
            },
            {
                icon: 'component3',
                title: 'CamDX members',
                meaning: 'are entities that wish to communicate with each other through CamDX. Each member connects with information systems of other members through a security server. Thus, all CamDX members need to add a security server, signed to CamDX\'s PKI, to their infrastructure.',
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