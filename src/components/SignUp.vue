<script setup>
import { useRouter } from "vue-router";
import {useAuth} from '../services/auth'

const router = useRouter();
const { register, loading, error } = useAuth()
 import { ref } from 'vue'

  const rules = {
    required: value => !!value || 'Required.',
    min: v => v.length >= 8 || 'Min 8 characters',
    passwordMatch: () => password === confirmPassword || `The passwords you entered don't match`,
  }

  const show1 = ref(false)
  const show2 = ref(true)
  const password = ref(null)  //password model
 

//   models
const firstName = ref(null)
const lastName = ref(null)
const email = ref(null)
const gender = ref(null)
const phoneNumber = ref(null)
const dateOfBirth = ref(null)
const gymLocations = ref(null)

const SignUp = async () => {

  loading.value = true;
  error.value = "";

  const formData = new FormData();
  formData.append("name", firstName.value +' '+ lastName.value,);
  formData.append("email", email.value);
  formData.append("phone", phoneNumber.value);
  formData.append("dateOfBirth ", dateOfBirth.value);
  formData.append("gender", gender.value);
  formData.append("gymLocations", gymLocations.value);
  formData.append("password", password.value);
  formData.append("role_id", 4);

  try {
    await register(formData)
   
    // Redirect after successful signup
    router.push('/homePage').then(() => {
        router.go(0); // Reloads the current route
    });
  } catch (err) {
    // Error is already handled by the auth service
    console.error('Sign up failed', err)
  }
};

  const confirmPassword = ref(null)
  const show1confirm = ref(false)
   


</script>

<template>
    
    <v-container width="60%">
        <v-row>
            <v-col md="12">
                <v-form>
                    
                        <v-col md="12" class="text-center">
                            <img src="/FullLogo_Transparent_NoBuffer.png" alt="MacFit Gym Logo" class="logo"  height="20%"  width="20%"/>
                        </v-col>

                    
                     <v-row>
                        <v-col class="text-center">
                            <div>Sign up  MacFit gym</div>
                        </v-col>
                     </v-row>

                    <v-row>
                        <v-col md="12" class="text-center">
                            <div  class="text-title-large font-weight-light text-medium text-left" >Firstname</div>
                        </v-col>
                        <v-col md="12">
                            <v-text-field variant="outlined" v-model="firstName"></v-text-field>
                        </v-col>
                    </v-row>

                    <v-row>
                        <v-col md="12" class="text-center">
                            <div  class="text-title-large font-weight-light text-medium text-left" >Lastname</div>
                        </v-col>
                        <v-col md="12">
                            <v-text-field variant="outlined" v-model="lastName"></v-text-field>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="12" class="text-center">
                            <div  class="text-title-large font-weight-light text-medium text-left" >Email</div>
                        </v-col>
                        <v-col md="12">
                            <v-text-field variant="outlined" v-model="email"></v-text-field>
                        </v-col>
                        
                    </v-row>
                    <v-row>
                        <v-col md="12" class="text-center">
                            <div  class="text-title-large font-weight-light text-medium text-left" >Date of birth</div>
                        </v-col>
                        <v-col md="6">
                            <v-date-input variant="outlined" v-model="dateOfBirth"></v-date-input>
                        </v-col>
                    </v-row>

                    <v-row>
                        <v-col md="12" class="text-center">
                            <div  class="text-title-large font-weight-light text-medium text-left" >Gender</div>
                        </v-col>
                        <v-col md="6">
                            <v-radio-group inline v-model="gender">
                                <v-radio label="Male" value="Male"></v-radio>
                                <v-radio label="Female" value="Female"></v-radio>
                            </v-radio-group>
                        </v-col>
                    </v-row>

                    <v-row>
                        <v-col md="12" class="text-center">
                            <div  class="text-title-large font-weight-light text-medium text-left" >Phone number</div>
                        </v-col>
                        <v-col md="12">
                            <v-text-field variant="outlined" v-model="phoneNumber"></v-text-field>
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
                                :rules="[rules.required, rules.min, rules.passwordMatch,]"
                                :type="show1 ? 'text' : 'password'"
                                variant="outlined"
                                @click:append="show1 = !show1"></v-text-field>
                        </v-col>
                    </v-row>

                    <v-row>
                        <v-col md="12" class="text-center">
                            <div class="text-title-large font-weight-light text-medium text-left">Confirm password</div>
                        </v-col>
                        <v-col md="12">
                            <v-text-field  
                                v-model="confirmPassword"
                                :append-icon="show1confirm ? 'mdi-eye' : 'mdi-eye-off'"
                                :rules="[rules.required, rules.min]"
                                :type="show1confirm ? 'text' : 'password'"
                                variant="outlined"
                                @click:append="show1confirm = !show1confirm"></v-text-field>
                        </v-col>
                    </v-row>


                      <v-row>
                        <v-col md="12" class="text-center">
                            <div  class="text-title-large font-weight-light text-medium text-left" >Gym locations</div>
                        </v-col>
                        <v-col md="6">
                                <v-select
                                    label="Select"
                                    :items="['CBD', 'Madaraka'  ,'Westlands', 'Buruburu',]"
                                    v-model="gymLocations"
                                  ></v-select>
                        </v-col>
                    </v-row>

                    <v-row>
                        <v-col md="4">
                            <v-btn color="#594976" variant="elevated" @click="SignUp">Sign Up</v-btn>
                        </v-col>
                    </v-row>

                    <v-row>
                        <v-col md="6">
                           <div>Already have an account? 
                                <router-link to="/login">Login</router-link>
                           </div>
                        </v-col>
                    </v-row>
                </v-form>
            </v-col>
        </v-row>
    </v-container>
</template>