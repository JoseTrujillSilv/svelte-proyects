<script>
  let hora = 0;
  let min = 0;
  let milisegundos = 0;
  let segundos = 0;
  let interval;
  let go = '';


  const iniciar = ()=>{
     go = 'GO!'
    interval = setInterval(start,1000);
  }



  const start = ()=>{
    milisegundos++;
    if (milisegundos===10) {
      milisegundos=0;
      segundos++;
    }

    if (segundos===6) {
      milisegundos=0;
      segundos=0;
      min++;
    }

    if (min===60) {
      milisegundos=0;
      segundos=0;
      min=0;
      hora++;
    }
  }

  const pause = ()=>{
    clearInterval(interval);
  }

  const stop = ()=>{
    clearInterval(interval);
    go = '';
    segundos = 0;
    milisegundos = 0;
    min = 0;
    hora = 0;
  }
</script>

<main>
    <div>
      <p class="go">{go}</p>
      <h1>CRONÓMETRO</h1>
    </div>
    <div>
      <p class="hora">{hora}:{min}<span class="segundos">{segundos}{milisegundos}</span></p>
    </div>
    <div>
      <button class="button-5" on:click={iniciar}>Iniciar</button><button class="button-5" on:click={pause}>Parar</button><button class="button-5" on:click={stop}>Restablecer</button>
    </div>
</main>

<style>
  main{display: flex;justify-content: center;align-items: center;gap: 30px;height: 100vh;flex-direction: column;}
  button{cursor: pointer;margin: 0px 20px;}
  .hora{font-size: 60px;}
  .segundos{font-size: 30px;}
  .go{color: green;text-align:center;font-size:80px;font-weight: bold;margin-bottom: 20px;}
 
.button-5 {
  align-items: center;
  background-clip: padding-box;
  background-color: #fa6400;
  border: 1px solid transparent;
  border-radius: .25rem;
  box-shadow: rgba(0, 0, 0, 0.02) 0 1px 3px 0;
  box-sizing: border-box;
  color: #fff;
  cursor: pointer;
  display: inline-flex;
  font-family: system-ui,-apple-system,system-ui,"Helvetica Neue",Helvetica,Arial,sans-serif;
  font-size: 16px;
  font-weight: 600;
  justify-content: center;
  line-height: 1.25;
  min-height: 3rem;
  padding: 10px 20px;
  position: relative;
  text-decoration: none;
  transition: all 250ms;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  vertical-align: baseline;
  width: auto;
}

.button-5:hover,
.button-5:focus {
  background-color: #fb8332;
  box-shadow: rgba(0, 0, 0, 0.1) 0 4px 12px;
}

.button-5:hover {
  transform: translateY(-1px);
}

.button-5:active {
  background-color: #c85000;
  box-shadow: rgba(0, 0, 0, .06) 0 2px 4px;
  transform: translateY(0);
}
</style>
