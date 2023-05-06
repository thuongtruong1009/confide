<script setup>
const loading = ref(false)
</script>


<template>
    <div>
        <MainSection title="Home" :loading="loading">
            content
        </MainSection>
    </div>
</template>