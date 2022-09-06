# Javascript - Eventos

## AddEventListener - click

~~~html
<body>
    <input type="text" id="meuId">
    <button id="btn-inc">Incrementa</button>

    <script>
      var meuInput = document.getElementById("meuId");
      var botaoInc = document.querySelector("#btn-inc") // ou document.getElementById("btn-inc")

      botaoInc.addEventListener('click', incrementa); // ao clicar no botão executa a função 'incrementa'

      function incrementa() {
          meuInput.value++;
      }
    </script>
</body>  
~~~

## Onclick

~~~html
<button onclick="this.innerHTML=Date()">The time is?</button>
~~~

## Onmouseover e Onmouseout

~~~javascript
function mouseMove(elemment) {
  elemment.innerHTML = "Obrigado.";
}

function mouseOut(elemment) {
  elemment.innerHTML = "Passe o mouse aqui.";
}
</script>
<p onmouseover="mouseMove(this)" onmouseout="mouseOut(this)">Passe o mouse aqui.</p>
~~~

## Onchange

~~~html
<script>
  function functionChange(elemment) {
    console.log(elemment.value);
  }
</script>

<select onchange="functionChange(this)">
  <option value="1">Value 1</option>
  <option value="2">Value 2</option>
  <option value="3">Value 3</option>
</select>
~~~

## Diversos Eventos

~~~javascript
onblur = alert("Hi");        
onselect = alert("Hi");      
onfocus = alert("Hi");       
onchange = alert("Hi");      
onclick = alert("Hi");       
onmouseover = alert("Hi");   
onmouseout = alert("Hi");    
onmousemove = alert("Hi");   
onmousedown = alert("Hi");   
onmouseup = alert("Hi");     
onkeydown = alert("Hi");     
onkeypmyStrs = alert("Hi");    
onkeyup = alert("Hi");       
onload = alert("Hi");        
onsubmit = alert("Hi"); 
~~~
