<template>
  <div>
    <Container>
      <ApartmentFilterForm
        class="apartments-filter"
        @submit="filter"/>
    </Container>
    <ApartmentsList :items="filteredApartments">
        <template v-slot:title> </template>
    </ApartmentsList>
  </div>
</template>

<script>

import ApartmentsList from './components/apartment/ApartmentsList'
import ApartmentFilterForm from './components/apartment/ApartmentFilterForm'
import apartments from './components/apartment/apartment'
import Container from './components/shared/Container'

export default {
  name: 'App',
  components: {
    ApartmentFilterForm,
    ApartmentsList,
    Container 
  },
  data() {
    return {
      text: '',
      apartments,
      filters: {
        city: '',
        price: 0
      }
    } 
  },
  computed: {
    filteredApartments() {
      return this.filterByCityName(this.filterByPrice(this.apartments))
    }
  },
  methods: {
    filter({city, price}) {
      this.filters.city = city
      this.filters.price = price
    },
    filterByCityName(apartments) {
      if(!this.filters.city) return apartments

      return apartments.filter(apartment => {
        return apartment.location.city === this.filters.city
      })
    },
    filterByPrice(apartments) {
      if(!this.filters.price) return apartments

      return apartments.filter(apartment => {
        return apartment.price >= this.filters.price
      })
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

