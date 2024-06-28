<script>

var classBox = 'box d-none';

const closeSidebar = ()=>{
    classBox = 'close-sidebar box';
}

const onSidebar = ()=>{
    classBox = 'box active-sidebar';
}

</script>

<div class="container">
    <div class="row">
      <div class="col"> 
        <button class="btn" on:click={onSidebar}><svg xmlns="http://www.w3.org/2000/svg" width="30" height="25" fill="currentColor" class="bi bi-list" viewBox="0 0 16 16">
            <path fill-rule="evenodd" d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5m0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5m0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5"/>
          </svg></button>
      </div>
    </div> 
    <div class="box-div">
        <div class={classBox}>
            <div class="row-btn">
                <div class="col">
                    <button style="background: none;
                border: none;" on:click={closeSidebar}><svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" class="bi bi-x-square-fill btn-close" viewBox="0 0 16 16">
                        <path d="M2 0a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V2a2 2 0 0 0-2-2zm3.354 4.646L8 7.293l2.646-2.647a.5.5 0 0 1 .708.708L8.707 8l2.647 2.646a.5.5 0 0 1-.708.708L8 8.707l-2.646 2.647a.5.5 0 0 1-.708-.708L7.293 8 4.646 5.354a.5.5 0 1 1 .708-.708"/>
                      </svg></button>
                </div>
            </div>
            <div class="row-h3">
                <div class="col">
                    <h3>Esto es un sidebar</h3>
                </div>
            </div>
        </div>
    </div>
  </div>



<style>

.row{
    display: flex;
    justify-content: end;
    padding: 20px;
  }

  .btn{
    background-color: #ffc107;
    padding: 5px;
    border: none;
    border-radius: 10px;
    cursor: pointer;
    font-weight: bold;
  }
  .btn:hover{
    box-shadow: orange 0px 1px 4px, orange 0px 0px 0px 3px;
  }

    .box{
        width: 300px;
        position: absolute;
        left: 0%;
        top: 0%;
        background-color: #ffc107;
        height: 100vh;
        box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px, rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;
    }
    .row-btn{
        text-align: end;
        padding: 20px;
    }
    .row-h3{
        text-align: center;
    }
    .btn-close{
        border-radius: 5px;
        cursor: pointer;
    }
    .btn-close:hover{
        box-shadow: rgba(6, 24, 44, 0.4) 0px 0px 0px 2px, rgba(6, 24, 44, 0.65) 0px 4px 6px -1px, rgba(255, 255, 255, 0.08) 0px 1px 0px inset;
    }

    .d-none{
        display: none;
    }

    
    .close-sidebar{
        animation: close 2s ease-in-out forwards;
    }

    .active-sidebar{
        animation: active 2s;
    }

  @keyframes active{
    0%{
      width: 0px;
    }
    100%{
      width: 300px;
    }
  }

  @keyframes close{
    0%{
      width: 300px;
    }
    100%{
      width: 0px;
      opacity: 0%;
    }
  }

</style>