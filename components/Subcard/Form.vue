<template>
    <form class="grid" @submit.prevent="backToFormPage">
        <input type="submit" value="Dismiss message" class="py-3.5 bg-[#242742] rounded-lg text-white cursor-pointer font-semibold">
    </form>
</template>

<script setup>
    const router = useRouter()
    const backToFormPage = () => {
        router.push("/")
    }
</script>