<script setup>
import "leaflet/dist/leaflet.css"
import * as L from 'leaflet';
import { ref, onMounted } from 'vue';

const initialMap = ref(null);

onMounted(()=> {
   initialMap.value = L.map('map1').setView([-1.2953145569779758, 36.817184449599566], 10);
   L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
       maxZoom: 19,
   }).addTo(initialMap.value);
   L.marker([-1.3073328374609299, 36.81211146039793]).addTo(initialMap.value);
});
    //    second map
onMounted(()=> {
   initialMap.value = L.map('map2').setView([-1.2953145569779758, 36.817184449599566], 10);
   L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
       maxZoom: 19,
   }).addTo(initialMap.value);
   L.marker([-1.3073328374609299, 36.81211146039793]).addTo(initialMap.value);
});
    //   third map
onMounted(()=> {
   initialMap.value = L.map('map3').setView([-1.2953145569779758, 36.817184449599566], 10);
   L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
       maxZoom: 19,
   }).addTo(initialMap.value);
   L.marker([-1.3073328374609299, 36.81211146039793]).addTo(initialMap.value);
});
    //   fourth map
onMounted(()=> {
   initialMap.value = L.map('map4').setView([-1.2953145569779758, 36.817184449599566], 10);
   L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
       maxZoom: 19,
   }).addTo(initialMap.value);
   L.marker([-1.3073328374609299, 36.81211146039793]).addTo(initialMap.value);
});
</script>

<template>
    <v-container mt="12">
        <v-row>
            <v-col>
                <div class="text-display-medium mb-6  ">Our location</div>
            </v-col>
        </v-row>

        <v-row>
            <v-col>
              <v-card>
                <v-row>

                    <v-col md="4">
                        <v-card-text>CBD</v-card-text>
                    </v-col>
                    <v-col md="8">
                        <div id="map1" style="height:30vh;"></div>
                    </v-col>

                </v-row>

              </v-card>
    
            </v-col>
            
        </v-row>

        <v-row>
            <v-col>
              <v-card>
                <v-row>

                    <v-col md="4">
                        <v-card-text>Madaraka</v-card-text>
                    </v-col>
                    <v-col md="8">
                        <div id="map2" style="height:30vh;"></div>
                    </v-col>

                </v-row>

              </v-card>
    
            </v-col>
            
        </v-row>

        <v-row>
            <v-col>
              <v-card>
                <v-row>

                    <v-col md="4">
                        <v-card-text>Westlands</v-card-text>
                    </v-col>
                    <v-col md="8">
                        <div id="map3" style="height:30vh;"></div>
                    </v-col>

                </v-row>

              </v-card>
    
            </v-col>
            
        </v-row>

        <v-row>
            <v-col>
              <v-card>
                <v-row>

                    <v-col md="4">
                        <v-card-text>Buruburu</v-card-text>
                    </v-col>
                    <v-col md="8">
                        <div id="map4" style="height:30vh;"></div>
                    </v-col>

                </v-row>

              </v-card>
    
            </v-col>
            
        </v-row>

    </v-container>

    <v-container  style="background-color:black "  max-width="100%" >
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
</template>