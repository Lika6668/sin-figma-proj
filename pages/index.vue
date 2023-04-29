<template>
  <v-col>
  <v-container>
    <v-col class="main-section" align="center">
      <video aria-label="Nothing great is made alone" 
        role="heading" aria-level="1" 
        src="https://cdn.sanity.io/files/599r6htc/localized/4caa8274fa1a76f5df188b7969c41e2b00890801.mp4" autoplay="" 
        playsinline="" class="main-video"></video>
      <h3>Figma connects everyone in the design process so teams can deliver better products, faster.</h3>
      <v-btn class="button"
        depressed color="primary" @click="scrollToForm">
        Get started
      </v-btn>
    </v-col>
    </v-container>
    <div>
      <img src="../static/main-img.png">
    </div>
    <v-container align="center">
    <SocialCard/>
    </v-container>
    <LastDivider/>
    <v-container ref="registerForm">
      <RegisterForm/>
    </v-container>
    </v-col>
</template>

<script>
import LastDivider from '~/components/LastDivider.vue';
import RegisterForm from '~/components/RegisterForm.vue';
import SocialCard from '~/components/SocialCard.vue';

export default {
   methods: {
      scrollToForm() {
        const el = this.$refs.registerForm;

        if (el) {
          el.scrollIntoView({ behavior: 'smooth'});
        }
      }
    }
}
</script>

 <style scoped>

.col {
  margin: 0;
  padding: 0;
 }

 .main-section {
    margin-bottom: 120px;
 }
 .main-video {
    max-width: 80%;
  }
  h3 {
    font-size: 20px;
    max-width: 500px;
    margin: 0px auto 40px;
    font-weight: 400;
  }

  img  {
    width: 110em;
    margin-left: -10%;
    margin-right: 0px;
  } 
</style>