<script setup>
import {
    Content,
    fetchOneEntry,
    isPreviewing,
    getBuilderSearchParams,
} from '@builder.io/sdk-vue';
import { onMounted, ref } from 'vue';


const BUILDER_PUBLIC_API_KEY = 'sdfgsdfgsdfgsdfg';
const content = ref(null);
const canShowContent = ref(false);
const model = 'page';


    content.value = await fetchOneEntry({
        model,
        apiKey: BUILDER_PUBLIC_API_KEY,
        options: getBuilderSearchParams(new URL(location.href).searchParams),
        userAttributes: {
            urlPath: window.location.pathname,
        },
    });
    canShowContent.value = content.value ? true : isPreviewing();
</script>


<template>


</template>

<style scoped>

</style>
