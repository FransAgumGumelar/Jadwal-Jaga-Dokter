<template>
  <v-navigation-drawer width="mx-auto" height="mx-auto" class="bg-red">
    <div align="center">
      <v-img
        class="mx-auto my-6"
        max-width="500"
        src="/public/logorssa.png"
      ></v-img>
  
      <v-card
            class="mx-auto pa-12 pb-8"
            elevation="8"
            max-width="448"
            rounded="lg"
          >
            <div class="text-subtitle-1 text-medium-emphasis">Username</div>
      
            <v-text-field
              density="compact"
              placeholder="Email address"
              prepend-inner-icon="mdi-email-outline"
              variant="outlined"
            ></v-text-field>
      
            <div class="text-subtitle-1 text-medium-emphasis d-flex align-center justify-space-between">
              Password
            </div>
      
            <v-text-field
              :append-inner-icon="visible ? 'mdi-eye-off' : 'mdi-eye'"
              :type="visible ? 'text' : 'password'"
              density="compact"
              placeholder="Enter your password"
              prepend-inner-icon="mdi-lock-outline"
              variant="outlined"
              @click:append-inner="visible = !visible"
            ></v-text-field>

      
            <v-btn
              class="mb-8"
              color="blue"
              size="large"
              variant="tonal"
              block
            >
              Log In
            </v-btn>

            <v-btn
              class="mb-8"
              color="blue"
              size="large"
              variant="tonal"
              block
            >
              Log In With Keycloak
            </v-btn>
      
            
      </v-card>
    </div>
  </v-navigation-drawer>
  </template>

  <script setup>
  definePageMeta({
  layout: 'login'
})

  </script>