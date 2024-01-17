<template>
  <div id="pagina">
    <SectionLeft></SectionLeft>
    <SectionRight></SectionRight>
  </div>
  <div class="footer_grande">
    <div class="footer">
      <div class="caja_footer">
        <SectionFooter iconFooter="fa-solid fa-fish" titFooter="Alimentación Saludable" pFooter="Comprende mejor tu peso en relación con tu altura utilizando nuestro índice de masa corporal (IMC)."/>
      </div>
    </div>
  <div class="footer">
    <div class="caja_footer">
      <SectionFooter iconFooter="fa-solid fa-football" titFooter="Hacer ejercicio" pFooter="Comprende mejor tu peso en relación con tu altura utilizando nuestro índice de masa corporal (IMC)."/>
    </div>
  </div>
    <div class="footer">
      <div class="caja_footer">
          <SectionFooter iconFooter="fa-solid fa-moon" titFooter="Dormir adecuadamente" pFooter="Comprende mejor tu peso en relación con tu altura utilizando nuestro índice de masa corporal (IMC)."/>
      </div>
    </div>
  </div>
</template>

<script>
import SectionLeft from '@/components/SectionLeft.vue';
import SectionRight from '@/components/SectionRight.vue';
import SectionFooter from '@/components/SectionFooter.vue';
export default {
  name: 'CabeceraIzquierda',
  components: {
    SectionLeft,
    SectionRight,
    SectionFooter
  }
}
</script>

<style lang="sass">
  *
    margin: 0
    padding: 0
  body
    background: radial-gradient(#D40280, #0C1113)
    background-size: cover
    background-attachment: scroll
    background-repeat: no-repeat
    min-height: 100vh
    font-family: 'Poppins', sans-serif
    overflow: hidden
  #pagina
    display: flex
  .footer_grande
    display: flex
  .footer
    display: flex
    flex-direction: column
    flex-wrap: wrap
    align-items: center
    justify-content: center
    margin-top: 2%
    .caja_footer
      background: #fff
      border-radius: 15px
      height: 175px
      width: 60%
      color: #333
      display: flex
      flex-direction: column

</style>
