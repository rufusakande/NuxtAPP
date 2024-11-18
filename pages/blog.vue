<template>
    <h1>Voir les articles</h1>
    <article v-for="post in poste" :key="post.id">
        <h2>{{ post.title }}</h2>
        <p>{{ post.body.slice(0, 100) }}</p>
        <p>
            <NuxtLink :to="`/${post.id}`">Lire la suite</NuxtLink>
        </p>
    </article>
</template>

<script setup>

const {data: poste} = useFetch('https://jsonplaceholder.typicode.com/posts?_limit=10')
</script>