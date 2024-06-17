<template>
    <form class="grid" @submit.prevent="validateEmail">
        <div>
            <div class="flex justify-between">
                <label class="text-xs font-semibold">Email address</label>
                <label v-if="isInvalid" class="text-xs font-semibold text-[#FF6257]">Valid email required</label>
            </div>
            <div class="grid">
                <input type="text" placeholder="email@company.com" v-model="email" :class="{'outline-[#FF6257] text-[#FF6257] bg-[#f9e8e7]':isInvalid, 'outline-[#9294A0]':!isInvalid}" class="outline outline-1 rounded-lg py-3 px-4 text-[#9294A0] mt-2"><br>
            </div>
        </div>
        <input type="submit" value="Subscribe to monthly newsletter" class="py-3.5 bg-[#242742] rounded-lg text-white cursor-pointer font-semibold">
    </form>
</template>

<script setup>
    const email = ref('')
    const isInvalid = ref(false)
    const router = useRouter()
    const validateEmail = () => {
        const regex = /^[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}$/i
        isInvalid.value = !regex.test(email.value)
        if (!isInvalid.value) {
            router.push({path: '/submission', query: {email: email.value}})
        }
    }
</script>