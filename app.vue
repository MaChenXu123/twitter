import { SidebarRight } from './.nuxt/components';
<template>
  <div :class="{ dark: dartMode }">
    <div class="bg-white dark:bg-dim-900">
      <div class="min-h-full">
        <div
          class="grid grid-cols-12 mx-auto xs:px-6 lg:max-w-7xl lg:px-8 lg:gap-5"
        >
          <!-- left -->
          <div class="hidden md:block xs:col-span-1 xl:col-span-2">
            <div class="sticky top-0">
              <Sidebar-Left></Sidebar-Left>
            </div>
          </div>
          <!-- main -->
          <!-- <div class="col-span-12 md:col-span-8 xl:col-span-6 bg-red-500">
asdsa
          </div> -->
          <!-- right -->
          <div class="col-span-12  md:block  xl:col-span-4 md:col-span-3 bg-blue-500">
            <div class="sticky top-0">
              <SidebarRight />
            </div>  
          </div>
        </div>
      </div>
    </div>
  </div>
  <div>
    <button @click="Huang">更换</button>
  </div>
</template>

<script setup>
const dartMode = ref(false);
const Huang = () => {
  console.log(dartMode.value);
  if (dartMode.value) {
    dartMode.value = false;
  } else {
    dartMode.value = true;
  }
};
</script>
