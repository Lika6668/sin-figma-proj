<template>
    <v-row justify='center'>
    <div class="form-section d-flex justify-center align-center">
    <v-col>
        <h2 class="text-register">Try Figma for free</h2>
        <v-form v-model="valid">
            <v-col align="center">
                <div class='form'>
            <v-text-field
            v-model="email"
            :rules="emailRules"
            label="E-mail"
            required
            ></v-text-field>

            <v-text-field
            v-model="password"
            :rules="passwordRules"
            label="Password"
            required
            ></v-text-field>
        </div>
            <v-btn outlined color="black">
              Create Account
            </v-btn>
        </v-col>
    </v-form>
           <p><small>By clicking "Create account", you agree to the <a>Figma</a> TOS and <a>Privacy Policy.</a></small></p> 
            <p><a>Use single sign-on</a></p>
           <p>Already have an account? <a>Log in</a></p> 
      
    </v-col>
</div>
</v-row>
</template>

<script>
 export default {
    data: () => ({
        valid: false,
        email: '',
        emailRules: [
            v => !!v || 'E-mail is requred',
            v => /.+@.+/.test(v) || 'E-mail must be ',
        ],
        password: '',
        passwordRules: [
            v => !!v || 'Password is required',
            v => v.length > 6 || 'Password must not be less, than 6 chars',
        ],
    }),
 }
</script>

    <style scoped>
    .form-section {
        height: 95vh;
        max-width: 400px;
    }

    .text-register {
        font-weight: 500;
        font-size: 35px;
        padding-bottom: 35px;
    }

    p, h2{
        text-align: center;
    }

    .form {
        padding-bottom: 35px;
    }
</style>