<script setup>
import { useRouter } from "vue-router";
const router = useRouter();
</script>
<template>
    <div>
        <h1>About</h1>
        <p>About Page Content</p>
        <a-button type="primary" class="w-40" @click="router.push('/')"
            >about page
        </a-button>
    </div>
</template>
