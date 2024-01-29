<template>
   <input type="text" class="serchText" v-bind="$attrs">
</template>

<script>

export default {
    name: 'CustomInput',

    model: {
        prop: 'value',
        event: 'input'
  },
} 


</script>

<style lang="scss" scoped>

</style>