<script setup>
const { defaultTransition, twitterBorderColor} = import('@/composable/useTailwindConfig.ts')
const wrapperClasses = computed(()=> `${defaultTransition} ${twitterBorderColor}`)
</script>


<template>
    <div class="p-3 hover:bg-gray-100 cursor-pointer dark:hover:bg-dim-300" :class="wrapperClasses">
        <slot></slot>
    </div>
</template>