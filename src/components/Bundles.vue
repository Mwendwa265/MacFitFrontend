<script setup>

</script>

<template >
    
    <v-container class="mt-10 p-10" style="background-color:#CFD0D6 " >
        <v-row class=" flex items-center justify-center ">
            <div class="text-display-medium mb-12 text-center w-full h-full ">Bundles and Pricing</div>
        </v-row>
        <v-row>
            
            <v-col md="3">
                <v-card class="text-center">
                    <v-icon color="#3A4B68" icon="mdi-clock-outline" size="large" class="mt-10"></v-icon>
                    <v-card-title color="#3A4B68">Daily Pass</v-card-title>
                    <v-card-text>600 Ksh</v-card-text>
                </v-card >
            </v-col>


            <v-col md="3">
                <v-card class="text-center">
                    <v-icon color="#3A4B68" icon="mdi-calendar-blank" size="large" class="mt-10"></v-icon>
                    <v-card-title color="#3A4B68">1 Month</v-card-title>
                    <v-card-text>1500 Ksh</v-card-text>
                </v-card>
            </v-col>


            <v-col md="3">
                <v-card class="text-center">
                    <v-icon color="#3A4B68" icon="mdi-dice-3" size="large" class="mt-10"></v-icon>
                    <v-card-title color="#3A4B68">3 Months</v-card-title>
                    <v-card-text>4500 Ksh</v-card-text>
                </v-card>
            </v-col>


            <v-col md="3">
                <v-card class="text-center">
                    <v-icon color="#3A4B68" icon="mdi-dice-6" size="large" class="mt-10"></v-icon>
                    <v-card-title color="#3A4B68">6 Months</v-card-title>
                    <v-card-text>9000 Ksh</v-card-text>
                </v-card>
            </v-col>
        </v-row>
        <v-row>
            
            <v-col md="12">
                <v-card class="text-center">
                    <v-icon color="#3A4B68" icon="mdi-dice-d12-outline" size="large" class="mt-10 "></v-icon>
                    <v-card-title color="#3A4B68">12 Months</v-card-title>
                    <v-card-text>18000 Ksh</v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </v-container>

    <!-- What's included -->
     <v-container class="mt-10 p-10" style="background-color:#CFD0D6 ">
        <v-row>
            <v-col md="12">
                <div class="text-display-medium mb-12 "> What's included in our bundle</div>
            </v-col>
        </v-row>

        <v-row>
            <v-col md="6">
                <v-card class="text-center">
                    <v-icon color="#3A4B68" icon="mdi-dumbbell" size="large" class="mt-10"></v-icon>
                    <v-card-title color="#3A4B68">state-of-the-art equipments</v-card-title>
                </v-card>
            </v-col>

            <v-col md="6">
                <v-card class="text-center">
                    <v-icon color="#3A4B68" icon="mdi-locker-multiple" size="large" class="mt-10"></v-icon>
                    <v-card-title color="#3A4B68">Storage for your belongings</v-card-title>
                </v-card>
            </v-col>

            <v-col md="6">
                <v-card class="text-center">
                    <v-icon color="#3A4B68" icon="mdi-fruit-watermelon" size="large" class="mt-10"></v-icon>
                    <v-card-title color="#3A4B68">We ensure you get the best diet</v-card-title>
                </v-card>
            </v-col>

            <v-col md="6">
                <v-card class="text-center">
                    <v-icon color="#3A4B68" icon="mdi-shower-head" size="large" class="mt-10"></v-icon>
                    <v-card-title color="#3A4B68">Clean and well maintained showers</v-card-title>
                </v-card>
            </v-col>

        </v-row>

        <v-row>
            <v-col md="6">
                <v-card class="text-center">
                    <v-icon color="#3A4B68" icon="mdi-account-group" size="large" class="mt-10"></v-icon>
                    <v-card-title color="#3A4B68">We ensure you enjoy together with others </v-card-title>
                </v-card>
            </v-col>
            <v-col md="6">
                <v-card class="text-center">
                    <v-icon color="#3A4B68" icon="mdi-cup-water" size="large" class="mt-10"></v-icon>
                    <v-card-title color="#3A4B68">Multiple water points</v-card-title>
                </v-card>
            </v-col>
        </v-row>
</v-container>

<!-- How to join -->
<v-container class="mt-10 p-10" style="background-color:#CFD0D6 ">
    <v-row>
        <v-col>
          <div>How to join</div>
        </v-col>
    </v-row>

    <v-row>
        <v-col>
            <v-list>
                <v-list-item>1.Select your prefered bundle</v-list-item>
                <v-list-item>2.Fill in the online application</v-list-item>
                <v-list-item>3.Make your payment</v-list-item>
                <v-list-item>4.Start you fitness journey</v-list-item>
            </v-list>
        </v-col>
    </v-row>
</v-container>
</template>