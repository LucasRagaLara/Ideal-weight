<template>
    <div class="cabecera">
        <img src="../assets/fitness.gif" alt="">
        <h1>CALCULA TU ÍNDICE<br> DE MASA CORPORAL</h1>
        <p>Comprende mejor tu peso en relación con tu altura utilizando nuestro índice de masa corporal (IMC). Si bien el IMC no es el único factor determinante de un peso saludable, proporciona un punto de partida valioso para evaluar tu salud y bienestar en general.</p>
    </div>
</template>

<script>
export default {
  data () {
    return {
        mensaje: "Esta es la cabecera componente"
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
  .cabecera
    border-radius: 0px 0px 40px
    width: 50%
    padding: 2% 10%
    display: flex
    flex-direction: column
    color: #fff
    height: 31.75rem
    background: linear-gradient(to bottom right, #FFFFFF, #710748)
    img
      width: 50%
    h1
      width: 100%
      letter-spacing: 1px
      margin: 3% 0
    p
      text-align: justify
      font-size: 18px
      width: 85%
</style>
