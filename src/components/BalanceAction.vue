<template>
  <button @click="action">{{ text }} Money</button>
</template>

<script>
export default {
    props: {
        text: String
    },
    methods: {
        action(){
            this.$emit('action')
        }
    }

}
</script>

<style>

</style>