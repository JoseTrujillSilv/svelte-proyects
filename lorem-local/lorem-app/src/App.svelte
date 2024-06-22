<script>
  let lorem = '';

  let valueInput;

  const words = [
  "amor",
  "alegría",
  "belleza",
  "bondad",
  "calidez",
  "cariño",
  "compasión",
  "confianza",
  "creatividad",
  "esperanza",
  "felicidad",
  "fortaleza",
  "generosidad",
  "humildad",
  "justicia",
  "libertad",
  "lealtad",
  "luz",
  "magia",
  "maravilla",
  "paz",
  "respeto",
  "sabiduría",
  "serenidad",
  "simplicidad",
  "sueño",
  "ternura",
  "valor",
  "verdad",
  "vida",
  "aventurero",
  "audaz",
  "brillante",
  "calmado",
  "carismático",
  "comprensivo",
  "corajoso",
  "creativo",
  "curioso",
  "dedicado",
  "divertido",
  "educado",
  "eficaz",
  "eficiente",
  "empático",
  "energético",
  "entusiasta",
  "fiable",
  "flexible",
  "fuerte",
  "generoso",
  "hábil",
  "honesto",
  "humilde",
  "idealista",
  "imaginativo",
  "independiente",
  "inteligente",
  "intrépido",
  "amable",
  "motivado",
  "optimista",
  "paciente",
  "pasional",
  "persistente",
  "positivo",
  "preciso",
  "profesional",
  "puntual",
  "responsable",
  "respetuoso",
  "seguro",
  "sencillo",
  "sensato",
  "servicial",
  "sincero",
  "simpático",
  "tolerante",
  "trabajador",
  "valiente",
  "visionario"
  ];

  const generate = () =>{
      lorem = '';
    for (let index = 0; index < valueInput; index++) {
      let roundNumber = Math.floor(Math.random() * (30 - 1 + 1)) + 1
      lorem += words[roundNumber]+' ';
    }
  }


 
</script>

<main>
  <div class="container">
    <h1>Lorem ipsum Aleatorio</h1>
    <div style="display: flex;gap: 20px;align-items: center;">
      <span style="font-weight: bold;">Palabras:</span>
      <input class="input" type="number" placeholder="0" name="num" id="num" bind:value={valueInput}>
      <button class="button-28" on:click={generate}>Generate</button>
    </div>
    <div>
      <p>{lorem}</p>
    </div>
  </div>
</main>

<style>
  .container{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    gap: 30px;
    padding: 16%;
  }
  p{
    width: 600px;
  }
 
  .button-28 {
    appearance: none;
    background-color: transparent;
    border: 2px solid #1A1A1A;
    border-radius: 10px;
    box-sizing: border-box;
    color: #3B3B3B;
    cursor: pointer;
    display: inline-block;
    font-family: Roobert,-apple-system,BlinkMacSystemFont,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol";
    font-weight: 600;
    line-height: normal;
    padding: 3px 10px;
    margin: 0;
    min-width: 0;
    outline: none;
    text-align: center;
    text-decoration: none;
    transition: all 300ms cubic-bezier(.23, 1, 0.32, 1);
    user-select: none;
    -webkit-user-select: none;
    touch-action: manipulation;
    will-change: transform;
  }

  .button-28:disabled {
    pointer-events: none;
  }

  .button-28:hover {
    color: #fff;
    background-color: #1A1A1A;
    box-shadow: rgba(0, 0, 0, 0.25) 0 8px 15px;
    transform: translateY(-2px);
  }

  .button-28:active {
    box-shadow: none;
    transform: translateY(0);
  }

  .input{
    box-sizing: border-box;
    font-family: inherit;
    font-size: 14px;
    vertical-align: baseline;
    font-weight: 400;
    line-height: 1.29;
    letter-spacing: .16px;
    border-radius: 0;
    outline: 2px solid transparent;
    outline-offset: -2px;
    width: 100px;
    height: 40px;
    border: none;
    border-bottom: 1px solid #8d8d8d;
    background-color: #f4f4f4;
    padding: 0 16px;
    color: #161616;
    transition: background-color 70ms cubic-bezier(.2,0,.38,.9),outline 70ms cubic-bezier(.2,0,.38,.9);  
  }

  .input:focus{
      outline: 2px solid #0f62fe;
      outline-offset: -2px;
  }


</style>
