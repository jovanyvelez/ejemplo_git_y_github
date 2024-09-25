<script lang="ts">

    let miTexto: HTMLInputElement;
    let cambio = false;

    function cambiar () {
        cambio ? miTexto.classList.remove('colorFondo'): miTexto.classList.add('colorFondo');

        cambio = !cambio;
        
    }

</script>

<form>
    <button onclick={()=> cambiar()}>Cambiar fondo</button>
    <input bind:this={miTexto} type="text" placeholder="pon tu texto acá" class="colorFondo miClase" id="miinput">
</form>

<style>
    .colorFondo {
        background-color: blanchedalmond;
    }

    .miClase {
        margin: 10px 0;
    }

    form {
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-top: 20px;
    }

</style>