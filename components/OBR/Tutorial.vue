<template>
    <v-card  class="rounded-0 pa-5" light>
        <v-container>
            <v-row v-for="(item, index) in items" :key="index" class="pa-5">
                <v-col cols="12">
                    <div class="titleSize text-left">
                        {{$t(item.question)}}
                    </div>
                </v-col>
                <v-col cols="12">
                    <!-- eslint-disable vue/no-v-html -->
                    <div class="subtitleSize text-left" v-html='$t(item.answer)'>
                    <!-- eslint-disable vue/no-v-html -->
                    </div>
                </v-col>
                <v-col cols="12" data-aos="zoom-in">
                <v-img class="img-fluid" :src="require('assets/' + item.image + '.png')" max-height="400px" :contain="true">
                </v-img>
                </v-col>
            </v-row>
        </v-container>
    </v-card>
</template>
<script>
export default {
    name: 'TutorialPage',
    data: () => ({
        items: [
            {
                image: 'tutor1',
                question: 'obrPage.howto.question1',
                answer: 'obrPage.howto.answer1'
            },
            {
                image: 'tutor2',
                question: 'obrPage.howto.question2',
                answer: 'obrPage.howto.answer2'
            },
            {
                image: 'tutor3',
                question: 'obrPage.howto.question3',
                answer: 'obrPage.howto.answer3'
            },
        ]
    }),
}
</script>
<style>
.white-button {
    background-color: white;
}
</style>