<script setup>
import { ref } from 'vue'
import { useRouter } from 'vue-router'

const router = useRouter()

  const rules = {
    required: value => !!value || 'Required.',
    min: v => v.length >= 8 || 'Min 8 characters',
    emailMatch: () => (`The email and password you entered don't match`),
  }

  const show1 = ref(false)
  const show2 = ref(true)
  const password = ref(null)
  const username = ref(null)


   function Login(){
    // retrive user details from local storage
 const userDetails = JSON.parse(localStorage.getItem('userDetails'))
 if(username.value == userDetails.email && password.value == userDetails.password){
         // proceed to home page
         localStorage.setItem('isLoggedIn', true)
            router.push('/home')    
    }else{
        console.log('Invalid username or password')
    }
       
   
}
</script>

<template>
    <v-container width="60%" mt="12">
        <v-row>
            <v-col md="12">
                <v-form>
                    
                        <v-col md="3" class="text-center">
                             <img src="/macfitLogo.png" alt="MacFit Gym Logo" class="logo"  height="20%" width="20%"/>
                        </v-col>

                     
                     <v-row>
                        <v-col class="text-center">
                            <div>Welcome to MacFit gym</div>
                        </v-col>
                     </v-row>

                     <v-row>
                        <v-col md="12" class="text-center">
                            <div  class="text-title-large font-weight-light text-medium text-left" >Username</div>
                        </v-col>
                        <v-col md="11">
                            <v-text-field v-model="username" label="Email" variant="outlined"></v-text-field>
                        </v-col>
                     </v-row>

                     <v-row>
                        <v-col md="12" class="text-center">
                            <div class="text-title-large font-weight-light text-medium text-left">Password</div>
                        </v-col>
                        <v-col md="12">
                            <v-text-field  
                                v-model="password"
                                :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
                                :rules="[rules.required, rules.min]"
                                :type="show1 ? 'text' : 'password'"
                                variant="outlined"
                              
                                counter
                                @click:append="show1 = !show1"></v-text-field>
                        </v-col>
                     </v-row>

                     <v-row>
                        <v-col md="4">
                            <v-btn color="black" variant="elevated" @click="Login">Login</v-btn>
                        </v-col>
                     </v-row>

                     <v-row>
                        <v-col md="6">
                            
                             <div>New to MacFit gym? 
                                <router-link to="/signup">sign Up</router-link>
                             </div>
                        </v-col>
                    </v-row>
                </v-form>
            </v-col>
        </v-row>
    </v-container>
</template>