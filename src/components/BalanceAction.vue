<template>
  <button :class="disable" @click="action" :disabled="disable">{{ text }} Money</button>
</template>

<script>
export default {
    props: {
        text: String,
        disable: {
            type: Boolean,
            default: false
        }
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