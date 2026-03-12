<script setup>
</script>
<template>
    <v-container max-width="100%">
        <v-row>
            <v-carousel>
                <v-carousel-item src="Fitness7.jpg" cover></v-carousel-item>
                <v-carousel-item src="Fitness8.jpg" cover></v-carousel-item>
                <v-carousel-item src="Fitness9.jpg" cover></v-carousel-item>
            </v-carousel>   
        </v-row>
    </v-container>

    <!-- About us -->
      <v-container max-width="100%"  style="background-color:#CFD0D6 ">
        <v-row >
            <v-col mb="8" class="text-center">
                <div class="text-display-medium mb-12">About us</div>
                <div class="text-title-large font-weight-light text-medium-emphasis mb-8">Welcome to <strong>MacFit GYM</strong> where we care about your fitness journey.Our gym is designed to be more than just a workout space it is a community where health, strength, and motivation come together.</div><br>

                <div class="text-title-large font-weight-light text-medium-emphasis mb-8">State of the art cardio machines (treadmills, bikes, rowers).We also have fully equipped strength-training zone with free weights and resistance machines,functional training area for HIIT, mobility, and core workouts and Spacious studio for group classes like yoga, spin, and aerobics </div><br>

                <div class="text-title-large font-weight-light text-medium-emphasis mb-8">Join us today and experience the difference.</div><br>
                <v-btn color="#594976">LEARN MORE</v-btn>
            </v-col>
        </v-row>
     </v-container class="d-flex align-center justify-center fill-height">


     <v-container>
        <v-row>
            <v-col md="4">
                <v-card>
                    <v-img src="Age.jpg" cover></v-img>
                    <v-card-title>We ensure healthy aging</v-card-title>
                    <v-card-text>Our programs are designed to help you maintain your health and vitality as you age.</v-card-text>
                    <v-btn color="#3A4B68">READ MORE</v-btn>
                </v-card>
            </v-col>
        
            <v-col md="4">
                <v-card>
                    <v-img src="Teamwork.jpg" cover></v-img>
                    <v-card-title>Teamwork</v-card-title>
                    <v-card-text>Working together towards common fitness goals.This creates a supportive and motivating environment for all .</v-card-text>
                    <v-btn color="#3A4B68">READ MORE</v-btn>
                </v-card>
            </v-col>

              <v-col md="4">
                <v-card>
                    <v-img src="Nutrition.jpg" cover></v-img>
                    <v-card-title>Nutrition</v-card-title>
                    <v-card-text>Proper nutrition is essential for achieving your fitness goals and maintaining a healthy lifestyle.</v-card-text>
                    <v-btn color="#3A4B68">READ MORE</v-btn>
                </v-card>
            </v-col>
        </v-row>
    </v-container>

    <!-- Reviews -->
    <v-container>
        <v-row>
            <v-col md="3"> 
                <v-card color="#CFD0D6">
                    <v-card-text>MacFit gym has the best trainers and equipment</v-card-text>
                    <v-rating length="5" :size="32" :model-value="2" active-color="primary"></v-rating>
                </v-card>
            </v-col>

              <v-col md="3"> 
                <v-card color="#CFD0D6">
                    <v-card-text>This has been the best fitness experience for me.</v-card-text>
                    <v-rating length="5" :size="32" :model-value="3" active-color="primary"></v-rating>
                </v-card>
            </v-col>

              <v-col md="3"> 
                <v-card color="#CFD0D6">
                    <v-card-text>For my family and I, MacFit has been a game-changer.</v-card-text>
                    <v-rating length="5" :size="32" :model-value="4" active-color="primary"></v-rating>
                </v-card>
            </v-col>

              <v-col md="3"> 
                <v-card color="#CFD0D6">
                    <v-card-text>MacFit has transformed my approach to fitness.</v-card-text>
                    <v-rating length="5" :size="32" :model-value="2" active-color="primary"></v-rating>
                </v-card>
            </v-col>
        </v-row>
    </v-container>

    <!-- Contact us -->
<v-container  style="background-color:#CFD0D6 "  max-width="100%" >
    <v-row >
        <v-col md="4" justify="center" align="center">   
            <v-icon color="#3A4B68" icon="mdi-phone" size="large" class="mt-10"></v-icon>
            <div   class="text-title-large font-weight-light text-medium-emphasis mb-8 ">Get in Touch:0722492864</div>
        </v-col>
        <v-col md="4" justify="center" align="center">
             <v-icon color="#3A4B68" icon="mdi-email" size="large" class="mt-10"></v-icon>
             <div   class="text-title-large font-weight-light text-medium-emphasis mb-8 ">macfit@example.com</div><br>
        </v-col>
        <v-col md="4" justify="center" align="center">
           <v-icon color="#3A4B68" icon="mdi-clock" size="large" class="mt-10"></v-icon>
           <div   class="text-title-large font-weight-light text-medium-emphasis mb-8 ">Opening hours : Mon-Fri: 5.00am-9.00pm | Sat: 5.30am-6.00pm | Sun:6.00am-6.00pm</div><br> 
        </v-col>
        <v-col md="4" justify="center" align="center">
            <v-icon color="#3A4B68" icon="mdi-map-marker" size="large" class="mt-10"></v-icon>
            <div   class="text-title-large font-weight-light text-medium-emphasis mb-8  ">MacFit GYM,4th floor J Mall,Nairobi</div><br>
        </v-col>
    </v-row>
</v-container>
</template>