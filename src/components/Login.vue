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

</script>

<template>
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
                            <div>Welcome to MacFit gym</div>
                        </v-col>
                     </v-row>

                    <v-row>
                        <v-col md="12" class="text-center">
                            <div  class="text-title-large font-weight-light text-medium text-center" >Username</div>
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