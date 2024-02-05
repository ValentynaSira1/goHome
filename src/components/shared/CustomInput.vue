<template>
   <input  
      v-model="text" 
      v-bind="$attrs" 
      
      class="custom-input" 
   >
</template>

<script>

export default {
    name: 'CustomInput',

    inheritAttrs: false,

    data() {
    return {
      text: ''
    } 
  }
} 


</script>

<style lang="scss" scoped>
@import '../../assets/scss/variables.scss';
.custom-input{
  height: 40px;
  max-width: 220px;
  width: 100%;
  border: 2px solid $main-color;
  font-size: 18px;
  outline: none;
  line-height: inherit;
  padding: 8px 15px;

  &::placeholder{
    color: inherit
  }
}
</style>