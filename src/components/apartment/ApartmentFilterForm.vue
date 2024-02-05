<template>
    <form class="form" @submit.prevent="handleSubmit">
        <CustomSelect 
            :items="cities"
            v-bind="$attrs" 
            v-model="city"
            class="form__select"
        />
        <CustomInput 
            placeholder="Цена, от"
            v-model="price"
        ></CustomInput>
        <SubmitButton 
            class="form__submit" 
            type="submit"
        >
            Подбор жилья
        </SubmitButton>
    </form>
</template>

<script>
import CustomSelect from '../shared/CustomSelect'
import CustomInput from '../shared/CustomInput'
import SubmitButton from '../PrimaryButton'

export default {
    components: {
        CustomSelect,
        CustomInput,
        SubmitButton
    },
    data() {
        return {
            price: 0,
            city: '',
        }; 
    },
    computed: {
        cities() {
            return  [
                {value: '', label: 'Город', selected: true},
                'Kyiv', 
                'Odesa', 
                'Poltava', 
                'Kharkiv', 
                'Dnipro', 
                'Lviv', 
                'Kherson', 
                'Mariupol'
            ];
        },
    },
    methods: {
        handleSubmit() {
            this.$emit('submit', {
                city: this.city, 
                price: this.price,
            });
        },
    },
  
};
</script>

<style lang="scss" scoped>
.form{
    display: flex;
    margin-bottom: 40px;

    &__select{
        margin-right: 30px;
    }
    &__submit{
        margin-left: auto;

    }
}
</style>