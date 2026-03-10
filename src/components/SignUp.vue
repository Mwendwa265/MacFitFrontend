<script setup>
 import { ref } from 'vue'

  const rules = {
    required: value => !!value || 'Required.',
    min: v => v.length >= 8 || 'Min 8 characters',
    emailMatch: () => (`The email and password you entered don't match`),
  }

  const show1 = ref(false)
  const show2 = ref(true)
  const password = ref(null)

  const confirmPassword = ref(false)
  const show1confirm = ref(true)
   


</script>

<template>
    <a href="Login.vue">SignUp</a>

    <v-container width="60%">
        <v-row>
            <v-col md="12">
                <v-form>
                    <v-row>
                        <v-col md="12" class="text-center">
                            <v-icon color="#3A4B68" icon="mdi-weight-lifter" size="large" class="mt-10"></v-icon>
                        </v-col>

                    </v-row>
                     <v-row>
                        <v-col class="text-center">
                            <div>Sign up  MacFit gym</div>
                        </v-col>
                     </v-row>

                    <v-row>
                        <v-col md="12" class="text-center">
                            <div  class="text-title-large font-weight-light text-medium text-center" >Firstname</div>
                        </v-col>
                        <v-col md="12">
                            <v-text-field></v-text-field>
                        </v-col>
                    </v-row>

                    <v-row>
                        <v-col md="12" class="text-center">
                            <div  class="text-title-large font-weight-light text-medium text-center" >Lastname</div>
                        </v-col>
                        <v-col md="12">
                            <v-text-field></v-text-field>
                        </v-col>
                    </v-row>
                    <v-row>
                        <v-col md="12" class="text-center">
                            <div  class="text-title-large font-weight-light text-medium text-center" >Email</div>
                        </v-col>
                        <v-col md="12">
                            <v-text-field></v-text-field>
                        </v-col>
                        
                    </v-row>
                    <v-row>
                        <v-col md="12" class="text-center">
                            <div  class="text-title-large font-weight-light text-medium text-center" >Date of birth</div>
                        </v-col>
                        <v-col md="6">
                            <v-date-input variant="outlined"></v-date-input>
                        </v-col>
                    </v-row>

                    <v-row>
                        <v-col md="12" class="text-center">
                            <div  class="text-title-large font-weight-light text-medium text-center" >Gender</div>
                        </v-col>
                        <v-col md="6">
                            <v-radio-group>
                                <v-radio label="Male" value="Male"></v-radio>
                                <v-radio label="Female" value="Female"></v-radio>
                            </v-radio-group>
                        </v-col>
                    </v-row>

                    <v-row>
                        <v-col md="12" class="text-center">
                            <div  class="text-title-large font-weight-light text-medium text-center" >Phone number</div>
                        </v-col>
                        <v-col md="12">
                            <v-text-field></v-text-field>
                        </v-col>
                    </v-row>

                    <v-row>
                        <v-col md="12" class="text-center">
                            <div class="text-title-large font-weight-light text-medium text-center">Password</div>
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
                        <v-col md="12" class="text-center">
                            <div class="text-title-large font-weight-light text-medium text-center">Confirm password</div>
                        </v-col>
                        <v-col md="12">
                            <v-text-field  
                                v-model="confirmPassword"
                                :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
                                :rules="[rules.required, rules.min]"
                                :type="show1confirm ? 'text' : 'password'"
                                variant="outlined"
                              
                                counter
                                @click:append="show1 = !show1"></v-text-field>
                        </v-col>
                    </v-row>
x

                      <v-row>
                        <v-col md="12" class="text-center">
                            <div  class="text-title-large font-weight-light text-medium text-center" >Gym locations</div>
                        </v-col>
                        <v-col md="6">
                                <v-select
                                    label="Select"
                                    :items="['CBD', 'Madaraka'  ,'Westlands', 'Buruburu',]"
                                 ></v-select>
                        </v-col>
                    </v-row>

                    <v-row>
                        <v-col md="4">
                            <v-btn color="#594976" variant="elevated">Login</v-btn>
                        </v-col>
                    </v-row>

                    <v-row>
                        <v-col md="6">
                            <div>New to MacFit gym? <a href="SignUp.vue">sign Up</a></div>
                        </v-col>
                    </v-row>
                </v-form>
            </v-col>
        </v-row>
    </v-container>
</template>