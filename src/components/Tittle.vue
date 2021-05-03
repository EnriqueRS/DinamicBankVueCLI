<template>
  <h1>{{ text }}</h1>
</template>

<script>
export default {
    name: 'Tittle',
    props: {
        text: String
    }
}
</script>

<style>
    h1 {
        color: peru
    }
</style>