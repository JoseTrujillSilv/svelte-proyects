<script>
  let color = 'red';
  let cont = 0;
  const arrayColor = [
  // Rojos
  "IndianRed",
  "LightCoral",
  "Salmon",
  "DarkSalmon",
  "LightSalmon",
  "Crimson",
  "Red",
  "FireBrick",
  "DarkRed",

  // Rosas
  "Pink",
  "LightPink",
  "HotPink",
  "DeepPink",
  "MediumVioletRed",
  "PaleVioletRed",

  // Naranjas
  "LightSalmon", // repeated from rojos
  "Coral",
  "Tomato",
  "OrangeRed",
  "DarkOrange",
  "Orange",

  // Amarillos
  "Gold",
  "Yellow",
  "LightYellow",
  "LemonChiffon",
  "LightGoldenrodYellow",
  "PapayaWhip",
  // ... (rest of the colors)
];


  const cambiaColor = ()=>{
      if (cont>arrayColor.length) {
        cont = 0;
      }
      color = arrayColor[cont];
      cont++;
  }

  

</script>

<main>
  <div class="container" style="background-color: {color};">
    <div class="h1-div">
      <h1>Background-color: {color}</h1>
    </div>
    <div>
      <button on:click={cambiaColor}>Cambiar Color</button>
    </div>
  </div>
</main>

<style>
  .container{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }
  .container>div{
    padding: 10px;
  }
  .h1-div{
    background-color: black;
    color: white;
    border-radius: 10px;
    font-family: Arial, Helvetica, sans-serif;
  }
  button{
    cursor: pointer;
    border: 2px solid black;
    background: none;
    padding: 10px 20px;
    font-family: Arial, Helvetica, sans-serif;
    font-weight: bold;
  }
  button:hover{
    background-color: black;
    color: white;
  }
</style>
