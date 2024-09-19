<template>
    <header>
        <h2>главная страница</h2>
    </header>
    <main>
        <article v-for="(post, index) in post" :key="post.id">
            {{ post.title }}
            <img src="https:" alt="">
            <ul>
                <li v-for="tag in post.tags" :key="tag.id">
                    {{ tag }}
                </li>
            </ul>
            <nuxt-linl to="/post/">подробнее</nuxt-linl>
        </article>
    </main>
</template>

<style scoped>
    main{
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 20px;
    }
    article{
        border-radius: 10px;
        background-color: brown;
        color: wheat;
        padding: 10px;

        display: flex;
        flex-direction: column;
        justify-content: space-between;
        
    }
    article ul{
        /* height: ; */
    }
    article img{
        width: 100%;
        height: 100px;
        object-fit: cover;
    }
    article a{
        padding: 10px;
        background-color: wheat;
        color: brown;
        text-decoration: none;
        text-align: center;
        display: block;
        border-radius: ;
    }
</style>

<script setup lang="ts">
  const dataTwice = await $fetch('https://dummyjson.com/posts')
  const post = dataTwice.post

</script>
