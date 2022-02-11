<template>
    <table>
        <TR>
            <TH> ID </TH>
            <TH> Наименование </TH>
            <TH> Артикул </TH>
            <TH> Категория </TH>
            <TH> Вес </TH>
            <TH> Себестоимость </TH>
            <TH> Состояние продукта </TH>
            <TH> Дата добавления </TH>
        </TR> 
        <mytabledata
        v-for="tt in tdata"
        v-bind:tt="tt"/>
    </table>
    


</template>

<script>
import  mytabledata from '@/components/mytabledata'

export default {
    props: ['tdata'],
    components: {
        mytabledata
    }
}
</script>
