<template>
    <v-card class="pa-10" dark color="#16184E">
        <v-container>
            <v-row align-self="center">
                <v-col cols="3"></v-col>
                <v-col cols="6" align="center">
                    <v-row>
                    <v-col cols="12" md="6" xs="12"  align="center">
                    <v-btn class="mr-1 " depressed filled color='primary' width="100%">
                        <v-icon class="mr-4">mdi-google-play</v-icon>
                        Android
                    </v-btn>
                </v-col>
                    <v-col cols="12" md="6" xs="12"  align="center">
                    <v-btn class="mr-1 " depressed filled color='primary' width="100%">
                        <v-icon class="mr-4">mdi-apple</v-icon>
                        IOS
                    </v-btn>
                </v-col></v-row>
            </v-col>
                <v-col cols="3"></v-col>
                <!-- <v-col cols="12" md="6" xs="12"  align="center">
                    <v-btn class="mr-1 " depressed filled color='primary' width="170px">
                        <v-icon class="mr-4">mdi-google-play</v-icon>
                        Android
                    </v-btn>
                </v-col>
                <v-col cols="12" md="6" xs="12"  align="center">
                    <v-btn class="mr-1 " depressed filled color='primary' width="170px">
                        <v-icon class="mr-4">mdi-apple</v-icon>
                        IOS
                    </v-btn>
                </v-col> -->
            </v-row>

            <v-row>

                <v-col cols="12">
                    <div class="md-2 text-center">
                        Development integration guides:
                    </div>
                </v-col>
            </v-row>

            <v-row cols="12">
                <v-col v-for="(item, index) in buttonItem" :key="index" cols="12" md="3" sm="6" xs="12" class="text-center">
                    <v-btn class="mr-1 " depressed light color='white' width="100%">
                    <v-icon class="mr-4">{{item.icon}}</v-icon>
                       {{item.label}}
                    </v-btn>
                </v-col>
            </v-row>
        </v-container>
    </v-card>
</template>
<script>
export default {
    name: 'GuidePage',
    data: () => ({
        buttonItem: [
            {
                icon: 'mdi-file-document',
                label: 'Documentation',
                link: ''
            },
            {
                icon: 'mdi-google-play',
                label: 'Android',
                link: ''
            },
            {
                icon: 'mdi-apple',
                label: 'IOS',
                link: ''
            },
            {
                icon: 'mdi-open-in-new',
                label: 'Web',
                link: ''
            }
        ]
    }),
}
</script>
<style>
.white-button {
    background-color: white;
}
</style>