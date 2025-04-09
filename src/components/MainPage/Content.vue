<template>
  <v-container>
    <v-card>
      <v-row>
        <v-col cols="1">
          <v-avatar
            v-if="hasProfileImage"
            :image="profileImage"
            color="surface-variant"
            size="75"
          ></v-avatar>
          <v-avatar v-else color="surface-variant" size="50">
            <v-icon size="35">mdi-account</v-icon>
          </v-avatar>
        </v-col>
        <v-col cols="10">
          {{ username }}
        </v-col>
        <v-col cols="1">
          <v-icon>mdi-dots-horizontal</v-icon>
        </v-col>
      </v-row>
      <v-divider></v-divider>

      <v-row>
        <v-col cols="12">
          <v-img
            src="../../assets/logo.svg"
            height="250"
            aspect-ratio="16/9"
          ></v-img>
        </v-col>
      </v-row>
      <v-divider></v-divider>
      <v-row justify="start">
        <v-col cols="auto" >
          <div>
            <v-icon :color="likeBtnColor" @click="onLike">{{ likeIcon }}</v-icon>
            <span>123</span>
          </div>
        </v-col>
        <v-col cols="auto">
          <div>
            <v-icon>mdi-chat-outline</v-icon>
            <span>123</span>
          </div>
        </v-col>
        <v-col cols="auto">
          <v-icon>mdi-send-variant-outline</v-icon>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>
<script setup lang="ts">
import { ref } from "vue";
const hasProfileImage = false;
const profileImage = computed(() => {
  return "";
});
const username = computed(() => {
  return "Jonathan";
});
const images = computed(() => {
  return [];
});

const likeBtnColor = ref("");
const hasLike = ref(false);
const likeIcon = ref("mdi-heart-outline");

function onLike(): void {
  hasLike.value = !hasLike.value;

  if (hasLike.value) {
    likeBtnColor.value = "red";
    likeIcon.value = "mdi-heart"
  }
  else{
    likeBtnColor.value = "";
    likeIcon.value = "mdi-heart-outline"
  }
}
</script>
