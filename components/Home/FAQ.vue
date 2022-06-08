<template>
    <v-card color="#F8F9FA" class="rounded-0 pa-10" light>
        <v-container>
            <v-row>
                <v-col cols="12">
                    <div class="text-h3 bold font-weight-medium text-center">
                        Frequently Asked Questions
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
                                    <v-list-item-title class="indigo--text">{{ item.question }}</v-list-item-title>
                                </v-list-item-content>
                            </template>

                            <v-list-item>
                                <v-list-item-content>
                                    {{ item.answer }}
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
                question: 'Does CamDX store the data?',
                answer: 'No. Security Servers at both side of communication do asymetric key encryption and digital signature that even CamDX cannot see or temper the content of the data exchange between two systems.',
            },
            {
                question: 'Why do I have to use CamDX if VPN can secure the channel?',
                answer: 'Attractions',
            },
            {
                question: 'Where is CamDX?',
                answer: 'Attractions',
            },
            {
                question: 'What kind of services that CamDX can offer?',
                answer: 'Attractions',
            },
            {
                question: 'How to join CamDX?',
                answer: 'Attractions',
            },
            {
                question: 'What are the benefit of joining CamDX?',
                answer: 'Attractions',
            },
        ],
    }),
}
</script>
<style>
</style>