<template>
    <div > 
        {{ props.title }}
    </div>
</template>

<script setup>
const props=defineProps({
    title:String,
    required:true, // 必须要给属性值
})
</script>