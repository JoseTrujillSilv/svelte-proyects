<script>
  let num = 0;
  let color = 'grey';

  const plus = ()=>{
    num++;
    colorNum();
  }

  const rest = ()=>{
    num--;
    colorNum();
  }

  const zero = ()=>{
    num = 0;
    colorNum();
  }

  const colorNum = ()=>{
    if (num<0) {
      color = 'red';
    }else if (num>0){
      color = 'green';
    }else{
      color = 'grey';
    }
  }


</script>

<main>

</main>
  <div class="container">
    <div>
      <h1>CONTADOR</h1>
    </div>
    <div>
      <p style="color: {color};">{num}</p>
    </div>
    <div style="display: flex; gap: 20px;">
      <button class="button-19" on:click={plus}>+</button>
      <button class="button-19" on:click={zero}>reset</button>
      <button class="button-19" on:click={rest}>-</button>
    </div>
  </div>
<style>
  .container{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    height: 100vh;
    gap: 20px;
  }
  button{
    cursor: pointer;
    padding: 10px 20px;
  }
  p{
    font-size: 160px;font-weight: bold;
  }
  h1{font-size: 80px;}

/* CSS */
.button-19 {
  appearance: button;
  background-color: #1899D6;
  border: solid transparent;
  border-radius: 16px;
  border-width: 0 0 4px;
  box-sizing: border-box;
  color: #FFFFFF;
  cursor: pointer;
  display: inline-block;
  font-family: din-round,sans-serif;
  font-size: 15px;
  font-weight: 700;
  letter-spacing: .8px;
  line-height: 20px;
  margin: 0;
  outline: none;
  overflow: visible;
  padding: 13px 16px;
  text-align: center;
  text-transform: uppercase;
  touch-action: manipulation;
  transform: translateZ(0);
  transition: filter .2s;
  user-select: none;
  -webkit-user-select: none;
  vertical-align: middle;
  white-space: nowrap;
  width: 100%;
}

.button-19:after {
  background-clip: padding-box;
  background-color: #1CB0F6;
  border: solid transparent;
  border-radius: 16px;
  border-width: 0 0 4px;
  bottom: -4px;
  content: "";
  left: 0;
  position: absolute;
  right: 0;
  top: 0;
  z-index: -1;
}

.button-19:main,
.button-19:focus {
  user-select: auto;
}

.button-19:hover:not(:disabled) {
  filter: brightness(1.1);
  -webkit-filter: brightness(1.1);
}

.button-19:disabled {
  cursor: auto;
}

.button-19:active {
  border-width: 4px 0 0;
  background: none;
}
</style>
