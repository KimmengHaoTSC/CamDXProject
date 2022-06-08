<template>
    <v-card  class="rounded-0 pa-10" light>
        <v-container>
            <v-row v-for="(item, index) in items" :key="index" class="pa-5">
                <v-col cols="12">
                    <div class="text-h3 bold font-weight-medium">
                        {{item.question}}
                    </div>
                </v-col>
                <v-col cols="12">
                    <div class="text-md" v-html="item.answer">
                        
                    </div>
                </v-col>
                <v-img :contain="true"  height="500" :src="require('assets/' + item.image + '.png')" width="100">
                        </v-img>
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
                question: 'How to Create an Account on CamDigiKey?',
                answer: "Go to CamDigiKey application, click the \"Register\" button and follow the instructions on the application."
            },
            {
                image: 'tutor2',
                question: 'How to Recover Your Existing Account on CamDigiKey?',
                answer: 'Click the "Recovery Existing Account" button, then enter the mobile phone number that you registered with the CamDigiKey application and enter the OTP code sent to the mobile phone number. Complete the process by going through some security steps including your personalized 6-digit pin code or biometric authentication and liveness face detection.'
            },
            {
                image: 'tutor3',
                question: 'How to Log into Portal/App with CamDigiKey?',
                answer: "<b>Web-based:</b> Go to a website that has been integrated with CamDigiKey application and scan the QR code that is shown on the website.<br><br><b>App-based:</b> Go to a mobile application that has been integrated with CamDigiKey application. After you click the “Login” button in the mobile application, you will receive a confirmation/rejection notification in the CamDigiKey application. Enter your personalized 6-digit pin code or biometric authentication to complete."
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