<template>
    <div class="sm:flex bg-white rounded-[30px] sm:w-[60rem] h-fit sm:justify-between sm:py-8 sm:pl-16 sm:pr-6 py-12">
        <div class="grid content-center gap-y-7 w-[25rem]">
            <div class="sm:text-6xl font-bold text-[#242742] text-5xl">
                <h1>Stay updated!</h1>
            </div>
            <div>
                <h1>Join 60,000+ product managers receiving monthly updates on:</h1>
            </div>
            <div class="grid gap-y-2">
                <CardList>
                    <h1>Product discovery and building what matters</h1>
                </CardList>
                <CardList>
                    <h1>Measuring to ensure updates are a success</h1>
                </CardList>
                <CardList>
                    <h1>And much more!</h1>
                </CardList>
            </div>
            <div>
                <CardForm></CardForm>
            </div>
        </div>
        <div class="hidden sm:block">
            <img src="public/assets/images/illustration-sign-up-desktop.svg">
        </div>
    </div>
    
</template>

<script setup>

</script>

