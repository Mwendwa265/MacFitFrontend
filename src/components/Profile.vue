<script setup>
const userDetails = JSON.parse(localStorage.getItem('user')) 

</script>

<template>
   <v-container width="50%" style="background-color: #CFD0D6;"class="mt-10 p-10" >
     <v-row>
        <v-col md="12">
            <v-card>
                <v-img src="" class="h-50" cover></v-img>
                <v-card-title>{{ userDetails.name }}</v-card-title>
                <v-card-text>{{ userDetails.email }}</v-card-text>
                <v-card-text>{{ userDetails.phoneNumber }}</v-card-text>
                <v-card-text>{{ userDetails.gymlocations}}</v-card-text>
                <v-card-text>{{ userDetails.gender}}</v-card-text>
                <div v-if="userDetails.subscription">
                <v-card-text>Your current subscriptions is: {{ userDetails.subscription.name}} at {{ userDetails.subscription.price }}  </v-card-text>
                </div>
                <div v-else>
                    <v-btn color="primary" variant="outlined" to="/bundles">bundles</v-btn>
                </div>


            </v-card>
        </v-col>
     </v-row>
   </v-container>
 

</template>