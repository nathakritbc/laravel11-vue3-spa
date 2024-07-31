<script setup>
import { ref } from "vue";
import { Button } from "ant-design-vue";
import { useRouter } from "vue-router";
const router = useRouter();
const message = ref("Hello World");
</script>
<template>
    <div>
        <h1>Home</h1>
        <p>Welcome to the Home Page</p>
        <h3>{{ message }}</h3>
        <button @click="router.push('/about')">about page</button>
        <Button type="primary">Test</Button>
        <a-button type="primary">Primary Button</a-button>
    </div>
</template>
