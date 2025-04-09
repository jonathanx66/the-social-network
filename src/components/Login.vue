<template>
  <v-img
    cover
    width="100vw"
    height="100vh"
    absolute
    style="z-index: 0"
    src="../../images/background_image_2.jpg"
  />

  <v-container
    style="z-index: 99"
    class="d-flex justify-center align-center h-screen elevation-1"
  >
    <v-card width="550" height="700" rounded="xl" color="white">
      <v-container height="300">
        <v-img
          cover
          width="550"
          height="300"
          absolute
          src="../../images/background-img.jpg"
        />
        <v-row no-gutters align="end" style="height: 200px" class="pl-10">
          <v-col>
            <div class="d-flex align-center h-100">
              <h2 class="text-h3 text-white">
                Welcome to<br />
                my social network
              </h2>
            </div>
          </v-col>
        </v-row>
      </v-container>

      <v-container height="300">
        <div class="d-flex justify-center pb-5">
          <h1>Login</h1>
        </div>

        <v-row no-gutters>
          <v-col cols="8" offset="2">
            <v-text-field label="Username"></v-text-field>
          </v-col>
        </v-row>

        <v-row no-gutters>
          <v-col cols="8" offset="2">
            <v-text-field label="Password"></v-text-field>
          </v-col>
        </v-row>

        <v-row no-gutters>
          <v-col cols="8" offset="2">
            <v-checkbox class="ml-n2 mt-n6" label="Remember me"></v-checkbox>
          </v-col>
        </v-row>

        <v-row no-gutters>
          <v-col cols="8" offset="2">
            <v-btn class="login-btn" @click="login">Login</v-btn>
          </v-col>
        </v-row>
      </v-container>
    </v-card>
  </v-container>
</template>
<script setup lang="ts">
import router from '@/router';



function login(): void{
  router.push("/main")
}
</script>
<style lang="scss">
.login-btn {
  background: rgb(2,0,36);
background: linear-gradient(90deg, rgba(2,0,36,1) 0%, rgba(121,9,97,1) 0%, rgba(0,212,255,1) 100%);
}
</style>