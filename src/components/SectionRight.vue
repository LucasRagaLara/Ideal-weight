<template>
    <div class="formulario">
        <img src="../assets/LUNGES_final.gif" alt="">
        <h1>INTRODUCE TUS DATOS</h1>
        <div>
            <div class="caja_inputs">
                <div class="inputs">
                    <label for="altura">Altura</label>
                    <input type="number" placeholder="Altura en cm" v-model="altura">
                </div>
                <div class="inputs">
                    <label for="altura">Peso</label>
                    <input type="number" placeholder="Peso en Kg" v-model="peso">
                </div>
            </div>
            <button id="calcular" @click="calcular">Calcular</button>
            <div class="mensaje">
                <h3>Bienvenido</h3>
                <p>Introduce tu peso y tu altura y verás el resultado de tu índice de masa corporal</p>
            </div>
        </div>
    </div>
</template>

<script>
import Swal from 'sweetalert2'
export default {
  data () {
    return {
        mensaje: "Este es el formulario del componente",
        altura: 0,
        peso: 0,
    }
  },
  methods: {
    calcular() {
        let altura_metros = this.altura / 100
        let resultado = this.peso / (altura_metros ** 2);
        if (resultado){
            Swal.fire({
        title: "Tu IMC es",
        text: resultado.toFixed(2),
        showClass: {
        popup: `
            animate__animated
            animate__fadeInUp
            animate__faster
        `
        },
        hideClass: {
        popup: `
            animate__animated
            animate__fadeOutDown
            animate__faster
        `
                }
            })
        }else{
            Swal.fire({
        title: "Tu IMC es",
        text: "No has rellenado todos los campos",
        showClass: {
        popup: `
            animate__animated
            animate__fadeInUp
            animate__faster
        `
        },
        hideClass: {
        popup: `
            animate__animated
            animate__fadeOutDown
            animate__faster
        `
                }
            })
            }
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
    .formulario
        display: flex
        align-items: center
        margin-top: 3vh
        flex-direction: column
        width: 50%
        color: #fff
        height: 31.75rem
        .caja_inputs
            display: flex
            align-items: center
            justify-content: center
        .inputs
            display: flex
            margin: 2% 5%
            flex-direction: column
            width: 50%
            input
                margin-top: 4%
                appearance: none
                outline: none
                padding: 10%
                text-align: center
                border: none
                border-radius: 15px
                font-size: 16px
                &::placeholder
                    font-style: italic
                    color: #222
                    letter-spacing: 2px
                    font-size: 16px
        #calcular
            border: none
            width: 20%
            border-radius: 10px
            color: #fff
            padding: 2%
            font-style: italic
            font-size: 16px
            background-color: #4D4D4D
            box-shadow: 4px 8px 4px 0px rgba(0, 0, 0, 0.25)
            margin: 3% 5%
            transition: ease-in-out
            transition-duration: 0.2s
            &:hover
                transform: scale(1.1)
        h1
            font-size: 45px
            letter-spacing: 2px
        img
            width: 17%
        .mensaje
            background: linear-gradient(to right, #E30088, rgba(0, 0, 0, 0.50))
            border-radius: 15px
            margin: 2% 5%
            padding: 5% 10%
            h3
                font-size: 24px
                margin-bottom: 2%
                letter-spacing: 2px
            p
                font-size: 16px
                font-style: italic
</style>
