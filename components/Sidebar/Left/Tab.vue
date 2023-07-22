<template>
  <nuxt-link
    to="#"
    class="flex items-center text-black p-3 w-min rounded-full hover:bg-gray-200 dark:hover:bg-dim-200 dark:text-white "
    :class="defaultTransition">
    <div class="w-6 h-6 text-dark">
      <!-- 用插槽来接受icon -->
      <slot name="icon"></slot>
    </div>
    <div class=" hidden ml-4   text-xl xl:block w-max" :class="textClasses">
      <!-- 用插槽来接受 导航名 -->
      <slot name="name"></slot>
    </div>
  </nuxt-link>
</template>

<script setup >
const {defaultTransition} =useTailwindConfig()
const props = defineProps({
  active: {
    type: Boolean,
    default: false
  },
});

const textClasses=computed(()=>{props.active ? 'font-semibold' : 'font-normal'})

</script>

