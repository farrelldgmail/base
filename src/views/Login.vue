<template>
    <v-form v-model="valid">
        <v-container>
            <v-row>
                <v-col
                    cols="12"
                ><h2>Login page</h2>
                </v-col>
            </v-row>
            <v-row>
                <v-col
                    cols="12"
                    md="6"
                >
                <v-text-field
                    v-model.trim="firstname"
                    :rules="nameRules"
                    label="First name"
                    required
                ></v-text-field>                
                </v-col>
                <v-col
                    cols="12"
                    md="6"
                >
                <v-text-field
                    v-model.trim="lastname"
                    :rules="nameRules"
                    label="Last name"
                    required
                ></v-text-field>                   
                </v-col>
            </v-row>

            <v-row>
                <v-col
                    cols="12"
                    md="6"
                ><v-btn to="../">Go back home</v-btn>
                </v-col>
                <v-col
                    cols="12"
                    md="6"
                ><v-btn :disabled="!valid" type="submit" >Login</v-btn>
                </v-col>
            </v-row>            
    
        </v-container>
    </v-form>
</template>

<script>
  /* Test */
  export default {
    data: () => ({
      valid: false,
      firstname: '',
      lastname: '',
      nameRules: [
        value => {
          if (value) return true
          return 'Name is requred.'
        },
      ],
    }),
  }
</script>
