<template>
    <v-card class="rounded-0 pa-10" light>
        <v-container>
            <v-row>
                <v-col cols="12">
                    <div class="text-h3 font-weight-medium text-center">
                        Design Principles
                    </div>
                </v-col>
                <v-col cols="12">
                    <div class="text-md subtitle md-2 text-center">
                        The design principle of CamDX adhering to the design concept of X-Road.
                    </div>
                </v-col>
            </v-row>
            <v-card-text>
                <v-row>
                    <v-col v-for="(item, index) in messages" :key="index" cols="12" md="4" sm="12" xs="12">
                    <div data-aos="flip-left">

                        <v-card-text>
                            <v-img :contain="true" height="100" :src="require('assets/' + item.avatar + '.png')"
                                width="100"></v-img>
                        </v-card-text>
                        <v-card-text class="text-h5 font-weight-bold">
                            {{ item.title }}
                        </v-card-text>
                        <v-card-text class="text-md">
                            {{ item.meaning }}
                        </v-card-text></div>
                    </v-col>
                </v-row>
            </v-card-text>
        </v-container>
    </v-card>
</template>
<script>
export default {
    name: 'DesignPropertypage',
    data: () => ({
        messages: [
            {
                avatar: 'design1',
                title: 'DISTRIBUTED',
                meaning: 'CamDX is a distributed system with no central database performing only data exchange.',
            },
            {
                avatar: 'design2',
                title: 'SECURE',
                meaning: 'Enterprise-class security at the application level by ensuring the authenticity, integrity and non-repudiation of the exchanged data.',
            },
            {
                avatar: 'design3',
                title: 'RELIABLE',
                meaning: 'No single point of failure. Failure could be partial. Each registry owner can employ proactive measures against any kinds of attack.',
            },
            {
                avatar: 'design4',
                title: 'DO NOT OWN DATA',
                meaning: 'CamDX neither store nore see the exchanged data. CamDX only captures meta-data for monitoring and reporting purpose.',
            },
            {
                avatar: 'design5',
                title: 'EASE OF USE',
                meaning: 'All communications in CamDX are based on web services, preferably REST API, and therefore can be used by all developers.',
            },
            {
                avatar: 'design6',
                title: 'Twitter',
                meaning: 'CamDX connects systems built on any platforms and technologies of choice.',
            },
        ],
    }),
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

.card-cus {
    border-color: rgba(210, 37, 37, 0.5);
    /* align-self:flex-start; */
    justify-items: left;
}
</style>