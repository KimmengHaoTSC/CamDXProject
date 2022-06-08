<template>
    <v-card class="rounded-0 pa-10" light>
        <v-container>
            <v-row>
                <v-col cols="12">
                    <div class="text-h3 font-weight-medium text-center">
                        Characteristics of Security Server
                    </div>
                </v-col>
                <v-col cols="12">
                    <div class="text-md subtitle md-2 text-center">
                        Acts as a bridge between two or more information systems engaging in secure data exchange.
                    </div>
                </v-col>
            </v-row>
            <v-row>
                <v-col cols="12" md="8" sm="12" xs="12" >
                    <v-row v-for="(item, index) in items" :key="index">
                        <v-col cols="2" md="2" sm="1" xs="1">
                            <v-img :src="require('assets/point.png')" :contain="true" width="30" height="30">
                            </v-img>
                        </v-col>
                        <v-col cols="10" md="8" sm="11" xs="11">
                            {{ item }}
                        </v-col>
                    </v-row>
                </v-col>
                <v-col cols="12" md="4" sm="12" xs="12" align="center">
                    <v-img :src="require('assets/secure.png')" :contain="true" height="400"></v-img>
                </v-col>
            </v-row>
        </v-container>
    </v-card>
</template>
<script>
export default {
    name: 'DesignPropertypage',
    data: () => ({
        items: [
            'Establishing a secure channel between two Security Servers in a manner that messages are encrypted, digitally signed and time-stamped to ensure the long-term authenticity value of the transaction',
            'Creating an overlay network among its peers over the Internet.',
            'Secured by Public Key Infrastructure (PKI).',
            'An API gateway with organizational-level access control.',
            'Handle multiple secure connections with its peers.'
        ]
    }),
}
</script>
<style>
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