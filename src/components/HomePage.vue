<script setup>
</script>
<template>
    <v-container fluid class="pa-0" >
        <v-row>
            <v-carousel>
                <v-carousel-item src="land1.jpg" cover></v-carousel-item>
                <v-carousel-item src="land2.jpg" cover></v-carousel-item>
                <v-carousel-item src="land3.jpg" cover></v-carousel-item>
            </v-carousel>   
        </v-row>
    </v-container>

     <!-- services -->
     <v-container max-width="100%"  style="background-color:#CFD0D6 ">
        <v-row >
            <v-col mb="8" class="text-center">
                <div class="text-display-medium mb-12">Our services</div>
                <div class="text-title-large font-weight-light text-medium-emphasis mb-8">Welcome to <strong>MacFit GYM</strong> where we care about your fitness journey.We offer a wide range of services to help you achieve your fitness goals.</div><br>

                <div class="text-title-large font-weight-light text-medium-emphasis mb-8">This services are designed to help you throughout you journey with us. </div><br>

                <div class="text-title-large font-weight-light text-medium-emphasis mb-8">Feel free to explore our offerings and find the perfect fit for your fitness needs and give us suggestions inorder to better you fitness journey.</div><br>
                <v-btn color="#594976">LEARN MORE</v-btn>
            </v-col>
        </v-row>
     </v-container class="d-flex align-center justify-center fill-height">


    <v-container>
        <v-row>
            <v-col md="6">
                <v-card>
                    <v-img src="yoga.jpg" cover></v-img>
                    <v-card-title>Yoga sessions</v-card-title>
                    <v-card-text>Join our yoga classes and improve your flexibility and strength</v-card-text>
                    <v-btn color="#B279A7">READ MORE</v-btn>
                </v-card>
            </v-col>
        
            <v-col md="6">
                <v-card>
                    <v-img src="menWorkoutSession.jpg" cover></v-img>
                    <v-card-title>Men's Workout Sessions</v-card-title>
                    <v-card-text>Join our targeted workout sessions designed specifically for men to build strength and improve fitness.</v-card-text>
                    <v-btn color="#B279A7">READ MORE</v-btn>
                </v-card>
            </v-col>

              <v-col md="12">
                <v-card >
                    <v-img src="womenWorkoutSession.jpg" cover></v-img>
                    <v-card-title>Women's Workout Sessions</v-card-title>
                    <v-card-text>Join our supportive workout sessions designed specifically for women to build confidence and improve fitness.</v-card-text>
                    <v-btn color="#B279A7">READ MORE</v-btn>
                </v-card>
            </v-col>
        </v-row>
    </v-container>

    <v-container  style="background-color:#CFD0D6 "  max-width="100%" >
       <v-row justify="center">
        <v-col md="4" >  
            <div   class="text-title-large font-weight-light text-medium-emphasis mb-8 mdi mdi-copyright" ><strong>MacFit GYM 2026</strong></div>
        </v-col>

       </v-row>
    </v-container>    
</template>
