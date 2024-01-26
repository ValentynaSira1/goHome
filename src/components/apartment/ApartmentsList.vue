<template>
    <ContainerS>
        <slot name="title"></slot>
        <div class="apartments-list">
            <ApartmentsItem 
                v-for="{id, descr, rating, imgUrl, price} in items"
                :key="id"
                :descr="descr"
                :price="price"
                :rating="rating"
                :imgSrc="imgUrl"
                class="apartments-list__item"
            />
        </div>
    </ContainerS>
</template>

<script>
import ApartmentsItem from './ApartmentsItem.vue'
import ContainerS from '../shared/Container.vue'

    export default {
        name: 'ApartmentsList',
        components: {
            ApartmentsItem,
                ContainerS,
           
        },
        props: {
            items: {
                type: Array,
                default: () => []
            }
        }
    }
</script>

<style lang="scss" scoped>
.apartments-list {
  display: flex;
  flex-wrap: wrap;
  margin-left: -15px;
  margin-right: -15px;

    &__item{
        margin-bottom: 30px;
        margin-left: 30px;
    }
}

</style>