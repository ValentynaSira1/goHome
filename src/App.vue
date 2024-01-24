<template>
 <ApartmentItem 
  :description="apartment.description"
  :price="apartment.price"
  :rating="apartment.rating"
  imgSrc="https://media.istockphoto.com/id/1415865722/photo/panoramic-view-of-lake-morskie-oko-or-eye-of-the-sea-tatra-mountains-near-zakopane-poland.webp?b=1&s=612x612&w=0&k=20&c=LmXMxzIyjyzBPKn9dtPGHc0e-ltQvRlfsh9YYUt6RSw="
 />
</template>

<script>

import ApartmentItem from './components/apartment/ApartmentItem.vue'


export default {
  name: 'App',
  components: {
    ApartmentItem
  },
  data() {
    return {
      apartment: {
        id: '5f689a2c09b16000e9a2f47b',
        title: 'Delectus et iste.',
        imgUrl: '/public/images/apartments/apartment5.jpg',
        description:
          'Debitis similique unde et eligendi sapiente in iure blanditiis distinctio. Cum nihil temporibus qui quam aut. Nesciunt qui eveniet eum quam voluptate numquam.',
        rating: 3,
        price: 1667,
        location: {
          city: 'Dnipro',
        },
        owner: {
          name: 'Bobbi',
          phone: '582-740-2926',
          email: 'Pete_Carter53@hotmail.com',
        }
      }
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
