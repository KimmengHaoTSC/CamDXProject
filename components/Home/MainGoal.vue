<template>
    <v-card class="rounded-0 pa-5 greybackground" light>
        <v-container>
            <v-card color="#C5C5C4" light class="bt-15" height="300"></v-card>
            <v-row>
                <v-col cols="12">
                    <div class="titleSize text-center pt-5">
                        {{ $t('homePage.camdxDetail.maingoalTitle') }}
                    </div>
                </v-col>
                <v-col cols="12">
                    <div class="subtitleSize text-center">
                        {{ $t('homePage.camdxDetail.maingoal') }}
                    </div>
                </v-col>
            </v-row>
        </v-container>
    </v-card>
</template>
<script>
export default {
    name: 'MainGoalpage'
}
</script>