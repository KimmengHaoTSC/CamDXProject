<template>
    <v-card color="#F8F9FA" class="rounded-0 pa-10" light>
        <v-container>
            <v-col cols="12">
                <v-row class="pb-5">
                    <v-col cols="12">
                        <div class="text-h3 bold font-weight-medium text-center">
                            Services Run Through CamDX
                        </div>
                    </v-col>
                </v-row>
                <v-col>
                    <v-row align="center">
                        <v-col v-for="(item, index) in items" :key="index" cols="12" md="4" sm="12">
                            <v-card class="card-cus justify-center box pa-1 " light height="350px">
                                <v-card color="primary" class="rounded-lg" height="200" dark>
                                    <v-card-title>
                                    </v-card-title>
                                    <v-card-text class="text-h5 font-weight-bold " color="white">
                                        {{ item.title }}
                                    </v-card-text>
                                </v-card>
                                <v-card-text class="text-md">
                                    {{ item.meaning }}
                                </v-card-text>
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
                title: 'Online Business Registration',
                meaning: 'a new business registration platform that combines at least four main relevant information systems into a single portal...',
            },
            {
                image: 'service2',
                title: 'Global Travel Assessment System ',
                meaning: 'a new business registration platform that combines at least four main relevant information systems into a single portal...',
            },
            {
                image: 'service3',
                title: 'Validation Application on Guarantee/Invitation',
                meaning: 'a new business registration platform that combines at least four main relevant information systems into a single portal...',
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