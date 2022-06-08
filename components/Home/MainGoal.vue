<template>
    <v-card color="#F8F9FA" class="rounded-0 pa-10" light>
        <v-container>
            <v-card color="#C5C5C4" light class="bt-15" height="300"></v-card>
            <v-row>
                <v-col cols="12" class="pa-10">
                    <div class="text-h3 bold font-weight-medium text-center">
                        The main goal of CamDX
                    </div>
                </v-col>
                <v-col cols="12">
                    <div class="text-md subtitle md-2 text-center">
                        To build an infrastructure that allows for establishing effortless access to data in government
                        databases (public services) without compromising the security and ownership of the data and with
                        minimal technical changes in the existing information systems.
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
</style>