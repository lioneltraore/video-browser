<template>
    <div>
        <input @input="onInput" />
    </div>
</template>


<script>
export default {
    methods: {
        onInput(ev) {
            console.log('search component: ', ev.target.value);
            this.$emit('termChange', ev.target.value);
        }
    }
}
</script>


<style>
    
</style>