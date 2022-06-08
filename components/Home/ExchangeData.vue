<template>
    <v-card color="#F8F9FA" class="rounded-0 pa-10" light>
        <v-container>
            <v-row>
                <v-col cols="12">
                    <div class="text-h3 bold font-weight-medium text-center">
                        Security of Data Exchange
                    </div>
                </v-col>
                <v-col cols="12">
                    <div class="text-md subtitle md-2 text-center">
                        A CamDX member does not require to develop its own solution ensuring the security and privacy of
                        the data. In CamDX, security of data exchange is ensured by distributed architecture, security
                        server and the use of standard technology.
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
                                        {{ item.title }}
                                    </v-card-text>
                                    <v-card-text class="text-md text-center">
                                        {{ item.meaning }}
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
                title: 'Confidentiality',
                meaning: 'Guaranteed with the condition that encrypted data are exchanged directly between members and do not pass through any third parties.',
            },
            {
                icon: 'exchange2',
                title: 'Availability',
                meaning: 'data exchange is practically independent of CamDX and its core components.',
            },
            {
                icon: 'exchange3',
                title: 'Integrity',
                meaning: 'CamDX is a distributed system with no central database performing only data exchange.',
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