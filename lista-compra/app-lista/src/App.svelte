<script>
  import Alert from './components/alert.svelte';
  import Box from './components/box.svelte';

  let actualComponent;
  let inputText;

  let components = [];

  const add = ()=>{
    components.push({itemText:inputText}); //Añadir nuevo componente con sus características nuevas
    actualComponent = Box; //Actualiza componente
  }

</script>

<main>
  <div>
    <Alert/>
  </div>
 <div class="container">
    <div>
      <h1>LISTA DE LA COMPRA</h1>
    </div>
    <div class="div-input">
      <input type="text" bind:value={inputText} name="item" id="item" placeholder="huevos..."><button class="button-68" on:click={add}>Add</button>
    </div>
    <div class="box-components">
      <!--------------------------------------------------------------------
      bind:this es esencial para que pueda indicarle que componente debe actualizar cuando se actualice arriba el componente: actualComponent
      ---------------------------------------------------------------------->
        {#each components as item} 
          <Box itemText={item.itemText} bind:this={actualComponent} inputText={inputText}/>
        {/each}
    </div>
 </div>
</main>

<style>
  .container{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 80vh;
    gap: 30px;
  }
  .div-input{
    display: flex;gap: 10px;
  }
  input{border-radius: 0px;padding: 5px;outline: none; border: none;border-bottom: 1px solid grey;}
  button{border-radius: 0px;cursor: pointer;padding: 5px 10px;outline: none;border: none;}


.button-68 {
  appearance: none;
  backface-visibility: hidden;
  background-color: rgb(46, 161, 255);
  border-radius: 8px;
  border-style: none;
  box-shadow: rgba(39, 174, 96, .15) 0 4px 9px;
  box-sizing: border-box;
  color: #fff;
  cursor: pointer;
  display: inline-block;
  font-family: Inter,-apple-system,system-ui,"Segoe UI",Helvetica,Arial,sans-serif;
  font-weight: 600;
  letter-spacing: normal;
  outline: none;
  overflow: hidden;
  padding: 10px 20px;
  position: relative;
  text-align: center;
  text-decoration: none;
  transform: translate3d(0, 0, 0);
  transition: all .3s;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  vertical-align: top;
  white-space: nowrap;
}

.button-68:hover {
  background-color: blue;
  opacity: 1;
  transform: translateY(0);
  transition-duration: .35s;
}

.button-68:active {
  transform: translateY(2px);
  transition-duration: .35s;
}

.button-68:hover {
  box-shadow: rgba(39, 174, 96, .2) 0 6px 12px;
}
.box-components{
  display: flex;
  flex-direction: column;
  gap: 20px;
}
</style>
