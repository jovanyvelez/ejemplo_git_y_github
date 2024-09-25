<script lang="ts">
    let miTexto: HTMLInputElement;
    let cambio = false;
</script>
<form>
    <button onclick={()=> cambio = !cambio}>Cambiar fondo</button>
    <input bind:this={miTexto} type="text" placeholder="pon tu texto acá" class="miClase" class:colorFondo={cambio}>
</form>

<style>
    .colorFondo {
        background-color: rgb(136, 111, 228);
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