<template>
    <TR>
            <TD> {{tt.id}} </TD>
            <TD> {{tt.name}} </TD>
            <TD> {{tt.artikul}} </TD>
            <TD> {{tt.category}} </TD>
            <TD> {{tt.weight}} </TD>
            <TD> {{tt.ownprice}} </TD>
            <TD> {{tt.status}} </TD>
            <TD> {{tt.adddate}} </TD>
    </TR>
    
</template>

<script >
export default {
    props: {
        tt: {
            type: Object,
            requred: true
        }
    }
}
</script>