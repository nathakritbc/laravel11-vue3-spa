<script setup>
import { ref, onMounted } from "vue";
import { useRouter } from "vue-router";
import axios from "axios";
const router = useRouter();
const message = ref("Hello World");

const getData = async () => {
    try {
        const { data, status } = await axios.get("/api/example");
        if (status === 200) {
            // message.value = data.message;
            console.log("data", data);
        }
    } catch (error) {
        console.error(error);
    }
};
onMounted(() => {
    getData();
});
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
