<template>
    <v-card color="#F8F9FA" class="rounded-0 pa-10" light>
        <v-container>
            <v-row>
                <v-col cols="12">
                    <div class="text-h3 bold font-weight-medium text-center">
                        {{ $t('homePage.faq.title') }}
                    </div>
                </v-col>
            </v-row>
            <v-col cols="12">
                <v-card v-for="(item, index) in items" :key="index" no-action class="mb-4">
                    <v-list>
                        <v-list-group>
                            <v-icon slot="prependIcon" large color="indigo darken-4">mdi-help-circle</v-icon>

                            <template #activator>
                                <v-list-item-content>
                                    <v-list-item-title class="indigo--text">{{ $t(item.question) }}</v-list-item-title>
                                </v-list-item-content>
                            </template>

                            <v-list-item>
                                <v-list-item-content>
                                    {{ $t(item.answer) }}
                                </v-list-item-content>
                            </v-list-item>
                        </v-list-group>
                    </v-list>
                </v-card>
            </v-col>
        </v-container>
    </v-card>

</template>
<script>
export default {
    name: 'FAQpage',
    data: () => ({
        items: [
            {
                question: 'homePage.faq.question1',
                answer: 'homePage.faq.answer1',
            },
            {
                question: 'homePage.faq.question2',
                answer: 'homePage.faq.answer2',
            },
            {
                question: 'homePage.faq.question3',
                answer: 'homePage.faq.answer3',
            },
            {
                question: 'homePage.faq.question4',
                answer: 'homePage.faq.answer4',
            },
            {
                question: 'homePage.faq.question5',
                answer: 'homePage.faq.answer5',
            },
            {
                question: 'homePage.faq.question6',
                answer: 'homePage.faq.answer6',
            },
        ],
    }),
}
</script>
<style>
</style>