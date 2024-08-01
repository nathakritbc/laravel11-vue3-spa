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
        <h1 class="text-3xl font-bold underline">Hello world!</h1>
        <section class="flex flex-col gap-2">
            <a-button type="primary" class="w-40" @click="router.push('/about')"
                >about page
            </a-button>
            <a-button type="primary" class="w-40">Primary Button</a-button>
        </section>
    </div>
</template>
