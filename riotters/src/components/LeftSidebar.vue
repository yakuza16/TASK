<script setup>
import UpperLogo from "./leftSidebarComponents/UpperLogo.vue";
import Menu from "./leftSidebarComponents/Menu.vue";
import BottomInfo from "./leftSidebarComponents/BottomInfo.vue";
import Avatar from "./leftSidebarComponents/Avatar.vue";
</script>

<template>
  <aside
    class="min-w-fit min-h-screen bg-[#F7F7F9] flex flex-col rounded-tl-3xl rounded-bl-3xl text-[#9896A1] px-1 md:px-8"
  >
    <UpperLogo />
    <Menu />
    <BottomInfo />
    <!-- just to show that I know what props is -->
    <Avatar name="Marc Webber" />
  </aside>
</template>

<style scoped></style>
