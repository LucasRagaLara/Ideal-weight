<template>
    <div class="footer">
        <i :class="iconFooter"></i>
        <h1>{{ titFooter }}</h1>
        <p>{{ pFooter }}</p>
    </div>
</template>

<script>
export default {
    name: "SectionFooter",
    props: {
        iconFooter: String,
        titFooter: String,
        pFooter: String
    },
    data () {
    return {
        mensaje: "Esta es la cabecera componente"
    }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
    i
        border-radius: 50%
        padding: 2%
        display: flex
        align-items: center
        justify-content: center
        width: 25px 
        height: 25px
        background-color: #333
        font-size: 20px
    .fa-fish
        background-color: #FF9292
        color: #4D1111
    .fa-football
        background-color: #FFE192
        color: #57471F
    .fa-moon
        background-color: #92BEFF
        color: #304C76
    h1
        margin: 2% 0
        font-size: 18px
    p
        font-size: 14px
        text-align: center
        width: 80%
</style>
