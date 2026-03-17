<script setup>
import { ref } from 'vue'
import {useRouter} from "vue-router";

const router = useRouter()

 const showBundleDialog = ref(false) 
 const isLoggedIn = localStorage.getItem('isLoggedIn')
 const selectedBundle = ref(null)
 const selectedPrice = ref(null)

function  showBundle(name,price){
    if(isLoggedIn){
        selectedBundle.value = name
        selectedPrice.value = price
        showBundleDialog.value = true
    }else{
        router.push('/login')
    }
}
 
function subscribe(){
    const userDetails = JSON.parse(localStorage.getItem('userDetails'))
    userDetails.subscription = {
        name: selectedBundle.value,
        price: selectedPrice.value,
    }
     localStorage.setItem('userDetails', JSON.stringify(userDetails))
     showBundleDialog.value = false
}

</script>

<template >
    
    <v-container class="mt-10 p-10" style="background-color:darkslategray"  >
        <v-row class=" flex items-center justify-center ">
            <div class="text-display-medium mb-12 text-center w-full h-full "><strong>Bundles and Pricing</strong></div>
        </v-row>
        <v-row>
             <div class="text-display-medium mb-12 text-center font-italic">click to subscribe</div>
        </v-row>
        <v-row>
            
            <v-col md="3">
                <v-card class="text-center" @click="showBundle('Daily pass', 600)">
                    <v-icon color="#3A4B68" icon="mdi-clock-outline" size="large" class="mt-10"></v-icon>
                    <v-card-title color="#3A4B68">Daily Pass</v-card-title>
                    <v-card-text>600 Ksh</v-card-text>
                </v-card >
            </v-col>


            <v-col md="3">
                <v-card class="text-center" @click="showBundle('1 month' ,1500)">
                    <v-icon color="#3A4B68" icon="mdi-calendar-blank" size="large" class="mt-10"></v-icon>
                    <v-card-title color="#3A4B68">1 Month</v-card-title>
                    <v-card-text>1500 Ksh</v-card-text>
                </v-card>
            </v-col>


            <v-col md="3">
                <v-card class="text-center" @click="showBundle('3 months', 4500)">
                    <v-icon color="#3A4B68" icon="mdi-dice-3" size="large" class="mt-10"></v-icon>
                    <v-card-title color="#3A4B68">3 Months</v-card-title>
                    <v-card-text>4500 Ksh</v-card-text>
                </v-card>
            </v-col>


            <v-col md="3">
                <v-card class="text-center" @click="showBundle('6 months',9000)">
                    <v-icon color="#3A4B68" icon="mdi-dice-6" size="large" class="mt-10"></v-icon>
                    <v-card-title color="#3A4B68">6 Months</v-card-title>
                    <v-card-text>9000 Ksh</v-card-text>
                </v-card>
            </v-col>
        </v-row>
        <v-row>
            
            <v-col md="12">
                <v-card class="text-center" @click="showBundle('12 months', 18000)">
                    <v-icon color="#3A4B68" icon="mdi-dice-d12-outline" size="large" class="mt-10 "></v-icon>
                    <v-card-title color="#3A4B68">12 Months</v-card-title>
                    <v-card-text>18000 Ksh</v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </v-container>

    <!-- What's included -->
     <v-container class="mt-10 p-10" style="background-color:darkslategray ">
        <v-row>
            <v-col md="12">
                <div class="text-display-medium mb-12 "> <strong>What's included in our bundle</strong></div>
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
<v-container class="mt-10 p-10" style="background-color:darkslategray">
    <v-row>
        <v-col>
          <div class="text-display-medium"><strong>How to join</strong></div>
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

<v-container  style="background-color:black "  max-width="100%" class="mt-10 p-10"  >
    <v-row >
        <v-col md="6" justify="center" align="center">   
            <v-icon color="#3A4B68" icon="mdi-phone" size="large" class="mt-10"></v-icon>
            <div class="text-white">Get in Touch:0722492864</div>
        </v-col>
        <v-col md="6" justify="center" align="center">
             <v-icon color="#3A4B68" icon="mdi-email" size="large" class="mt-10"></v-icon>
             <div   class="text-white">macfit@example.com</div><br>
        </v-col>
        <v-col md="6" justify="center" align="center">
           <v-icon color="#3A4B68" icon="mdi-clock" size="large" class="mt-10"></v-icon>
           <div   class="text-white">Opening hours : Mon-Fri: 5.00am-9.00pm | Sat: 5.30am-6.00pm | Sun:6.00am-6.00pm</div><br> 
        </v-col>
        <v-col md="6" justify="center" align="center">
            <v-icon color="#3A4B68" icon="mdi-map-marker" size="large" class="mt-10"></v-icon>
            <div  class="text-white">MacFit GYM,4th floor J Mall,Nairobi</div><br>
        </v-col>
    </v-row>
</v-container>

      <!-- dialog -->
  <v-dialog v-model="showBundleDialog" max-width="600" >

      <v-card prepend-icon="mdi-account" title="Subscribe to Bundle" >
        <v-card-text>
          You are about to subscribe to {{ selectedBundle }} at {{ selectedPrice }}. Click on the button below to complete payment
        </v-card-text>

        <v-divider></v-divider>
    <v-card-actions>
         <v-spacer></v-spacer>
          <v-btn text="Close" variant="plain" @click="showBundleDialog = false" ></v-btn>
          <v-btn color="primary" variant="tonal" @click="subscribe()" >Subscribe</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
</template>