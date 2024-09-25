<script lang="ts">

    let miTexto: HTMLInputElement;
    let cambio = false;

    $effect(() => {
        miTexto = document.getElementById('miinput') as HTMLInputElement;
    })

    function cambiar () {
        cambio ? miTexto.classList.remove('colorFondo'): miTexto.classList.add('colorFondo');

        cambio = !cambio;
        
        //si queremos cambiar el color de fondo del body
    }

</script>

<form>
    <button onclick={()=> cambiar()}>Cambiar fondo</button>
    <input type="text" placeholder="pon tu texto acá" class="colorFondo miClase" id="miinput">
</form>

<style>
    .colorFondo {
        background-color: aquamarine;
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