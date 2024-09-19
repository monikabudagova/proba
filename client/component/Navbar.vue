<template>
    <nav>
        <li><nuxt-link to="/">home</nuxt-link></li>
        <li><nuxt-link to="/about">about</nuxt-link></li>
        <li><nuxt-link to="/contact">contact</nuxt-link></li>
    </nav>
</template>
<style scoped>
    ul{
        display: flex;
        gap: 10px;
        list-style: none;
    }
</style>