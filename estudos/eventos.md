# Javascript - Eventos

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

## On click

~~~html
<button onclick="this.innerHTML=Date()">The time is?</button>
~~~

## On mouse over e On mouse out

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

## On change

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
