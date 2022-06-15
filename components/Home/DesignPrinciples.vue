<template>
    <v-card class="rounded-0 pa-5" light>
        <v-container>
            <v-row>
                <v-col cols="12">
                    <div class="titleSize text-center">
                        {{ $t('homePage.principles.title') }}
                    </div>
                </v-col>
                <v-col cols="12">
                    <div class="subtitleSize md-2 text-center">
                        {{ $t('homePage.principles.subtitle') }}
                    </div>
                </v-col>
            </v-row>
            <v-card-text>
                <v-row>
                    <v-col v-for="(item, index) in messages" :key="index" cols="12" md="4" sm="6" xs="6">
                    <div data-aos="flip-left">

                        <v-card-text align="center">
                            <v-img 
                                :contain="true" height="100" :src="require('assets/' + item.avatar + '.png')"
                                width="100"></v-img>
                        </v-card-text>
                        <v-card-text class="subtitleSize font-weight-bold " align="center">
                            {{ $t(item.title) }}
                        </v-card-text>
                        <v-card-text class="textSize ">
                            {{ $t(item.meaning) }}
                        </v-card-text></div>
                    </v-col>
                </v-row>
            </v-card-text>
        </v-container>
    </v-card>
</template>
<script>
export default {
    name: 'DesignPrinciplepage',
    data: () => ({
        messages: [
            {
                avatar: 'design1',
                title: "homePage.principles.distributed.title",
                meaning: "homePage.principles.distributed.meaning",
            },
            {
                avatar: 'design2',
                title: "homePage.principles.secure.title",
                meaning: "homePage.principles.secure.meaning",
            },
            {
                avatar: 'design3',
                title: "homePage.principles.reliable.title",
                meaning: "homePage.principles.reliable.meaning",
            },
            {
                avatar: 'design4',
                title: "homePage.principles.notowndata.title",
                meaning: "homePage.principles.notowndata.meaning",
            },
            {
                avatar: 'design5',
                title: "homePage.principles.easeofuse.title",
                meaning: "homePage.principles.easeofuse.meaning",
            },
            {
                avatar: 'design6',
                title: "homePage.principles.last.title",
                meaning: "homePage.principles.last.meaning",
            },
        ],
    }),
}
</script>