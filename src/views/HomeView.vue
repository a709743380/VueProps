<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld :msg="myData.msg" />
    <AboutView v-model="myData.msg" />
    <AboutViewOP v-model="myData.msg" />
  </div>
</template>

<script setup lang="ts">
// 引入 Vue
import { defineComponent, reactive } from "vue";
import HelloWorld from "@/components/HelloWorld.vue"; // 假設 HelloWorld 組件位於相同目錄下
import AboutView from "./AboutView.vue"; // 假設 HelloWorld 組件位於相同目錄下
import AboutViewOP from "@/views/AboutViewOP.vue"; // 假設 HelloWorld 組件位於相同目錄下
import { HomeData } from "@/interfaces/HomeData"; // 假設 HelloWorld 組件位於相同目錄下

const myData: HomeData = reactive({
  msg: "Hello from HomeData!",
});
</script>
