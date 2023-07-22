<template>
  <div class="flex flex-col h-screen">
    <div
      class="rounded-full p-2 my-2 hover:rounded-full hover:bg-yellow-200 w-min dark:hover:bg-white/20"
      :class="defaultTransition"
    >
      <nuxt-link to="/">
        <div class="w-8 h-8">
          <LogoTwitter></LogoTwitter>
        </div>
      </nuxt-link>
    </div>
    <div class="mt-2 space-y-3">
      <SidebarLeftTab active>
      <template #icon>
        <HomeIcon />
      </template>
      <template #name> 首页 </template>
    </SidebarLeftTab>
    <SidebarLeftTab active>
      <template #icon>
        <HomeIcon />
      </template>
      <template #name> 首页 </template>
    </SidebarLeftTab>
    <SidebarLeftTab active>
      <template #icon>
        <HomeIcon />
      </template>
      <template #name> 首页 </template>
    </SidebarLeftTab>
    <SidebarLeftTab active>
      <template #icon>
        <HomeIcon />
      </template>
      <template #name> 首页 </template>
    </SidebarLeftTab>
    </div>
  </div>
</template>

<script setup>
import { HomeIcon } from "@heroicons/vue/solid";
const { defaultTransition } = useTailwindConfig();
</script>
