# Broken

Install Dependencies and run npm run build

Visit the home page which is resources/Pages/Welcome.vue

Will return error Unable to locate file in Vite manifest: resources/js/Pages/Welcome.vue.

Removing import { Content, fetchOneEntry, isPreviewing, getBuilderSearchParams } from '@builder.io/sdk-vue';from Welcome.vue results in working builds but not working Builder.IO.
