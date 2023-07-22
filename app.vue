<template>
  <div :class="{ dark: dartMode }">
    <div class="bg-white dark:bg-dim-900">
      <div class="min-h-full">
        <div
          class="grid grid-cols-12 mx-auto xs:px-6 lg:max-w-7xl lg:px-8 lg:gap-5"
        >
          <!-- left -->
          <div class=" md:block xs:col-span-1 xl:col-span-2">
            <div class="sticky top-0">
              <Sidebar-Left></Sidebar-Left>
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
const Huang=()=>{
  console.log(dartMode.value);
  if(dartMode.value){
    dartMode.value=false
  }else{
    dartMode.value=true
  }
}
</script>
