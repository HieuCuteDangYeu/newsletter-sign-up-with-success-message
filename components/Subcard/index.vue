<template>
    <div class="grid bg-white rounded-[30px] h-fit w-[31rem] gap-10 p-16">
        <div>
            <img src="public/assets/images/icon-success.svg">
        </div>
        <div class="text-6xl text-[#242742] font-bold">
            <h1>Thanks for subscribing!</h1>
        </div>
        <div class="text-[#242742]">
            <p>A confirmation email has been sent to {{ emailFromQuery }}. Please open it and click the button inside to confirm your subscription.</p>
        </div>
        <div>
            <SubcardForm></SubcardForm>
        </div>
    </div>
</template>

<script setup>
    const route = useRoute()
    const emailFromQuery = route.query.email
</script>