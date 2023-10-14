<template>
  <div class="home-page">
    <h1>{{ pageTitle }}</h1>
    <Button buttonName="Go to about page by action" @click="goToAboutPage" />
    <Button
      style="margin-top: 5px"
      buttonName="Change page title"
      @click="changePageTitle('Our very new title')"
    />
    <router-link to="/about">Go to home page by link</router-link>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";
import { useRouter } from "vue-router";
import Button from "@/components/ui/Button.vue";

const pageTitle = ref<string>("Home page");

const router = useRouter();

function goToAboutPage() {
  router.push("/about");
}

function changePageTitle(newTitle: string) {
  pageTitle.value = newTitle;
}
</script>

<style lang="scss"></style>
