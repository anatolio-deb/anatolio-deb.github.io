<template>
  <v-container>
    <Label />
    <v-row>
      <v-col cols="5"></v-col>
      <v-col cols="1">
        <v-btn rounded="xl" size="large" color="indigo-lighten-4" variant="tonal" @click="toTry">
          Try
        </v-btn>
      </v-col>
      <v-col cols="6">
        <v-btn rounded="xl" size="large" color="cyan-lighten-4" variant="tonal" @click="toBuy">
          Buy
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup lang="ts">
import { useRoute, useRouter } from "vue-router";
import Label from "./Label.vue";
// import Logo from "../components/Logo";
const route = useRoute();
const router = useRouter();

function toTry() {
  router.push("/try");
}
function toBuy() {
  router.push("/buy");
}
</script>
