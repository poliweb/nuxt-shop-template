<template>
    <section class="bg-white">
        <div class="container px-5 py-3 mx-auto flex items-center justify-between">
            <!-- Logo -->
            <NuxtLink to="/">
                <Logo />
            </NuxtLink>
            <!-- Menu -->
            <div class="flex items-center gap-x-[30px]">
                <NuxtLink v-for="item in menuItems" :key="item.index" :to="item.link" class="uppercase text-sm">{{ item.name
                }}</NuxtLink>
            </div>
            <!-- Icons -->
            <div class="flex items-center gap-x-[25px]">
                <IconsUser />
                <IconsFavorite />
                <IconsCart />

            </div>
        </div>
    </section>
</template>

<script setup>

const menuItems = [
    {
        link: '/',
        name: 'главная'
    },
    {
        link: '/catalog',
        name: 'каталог'
    },
    {
        link: '/collections',
        name: 'коллекции'
    },
    {
        link: '/sale',
        name: 'распродажа'
    },
    {
        link: '/contacts',
        name: 'контакты'
    },
]

</script>

<style scoped></style>