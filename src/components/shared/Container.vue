<template>
    <div class="container">
        <slot> </slot>
    </div>
</template>

<script>
    export default {
        name: 'ContainerS'
    }
</script>

<style lang="scss" scoped>
.container{
    max-width: 1100px;
    margin: 0 auto;
}
</style>