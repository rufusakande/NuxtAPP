<template>
    <main>
        <h1>{{ post.title }}</h1>
        <p>{{ post.body }}</p>

    </main>
</template>

<script setup>
    const root = useRoute()
    const {data: post} = useFetch(() =>"https://jsonplaceholder.typicode.com/posts/"+ root.params.id)
</script>