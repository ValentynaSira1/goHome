<template>
  <div>
    <CustomInput v-model="serchText"/>
    {{serchText}}
    <ApartmentsList :items="apartments">
        <template v-slot:title> New title</template>
    </ApartmentsList>
  </div>
</template>

<script>

import ApartmentsList from './components/apartment/ApartmentsList.vue'
import CustomInput from './components/shared/CustomInput.vue'
import apartments from './components/apartment/apartment'

export default {
  name: 'App',
  components: {
    ApartmentsList, 
    CustomInput
  },
  data() {
    return {
      serchText: '',
      apartments
    } 
  }
  
}
</script>

<style>
#app {
  font-family: Montserrat, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
Vue.version

