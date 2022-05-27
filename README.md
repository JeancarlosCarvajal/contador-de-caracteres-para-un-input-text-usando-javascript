# contador-de-caracteres-para-un-input-text-usando-javascript
Contador de Caracteres para un Input Text usando JavaScript
 
 
 
   <body> 
      <div style="display: inline-grid;"> 
         <input type="text" id="input"> 
         <strong>Input Vacío, 20 caracteres Máximo</strong>
      </div>  
   </body> 

   <script> 
      // Evento que lee el input
      document.getElementById('input').addEventListener('input', function(e) {
         // EL target del evento es el elemento Input
         var input = e.target;
         // Establecemos el maximo de caracteres permitidos
         var max = 20;
         // Leemos la cantidad de caracteres en el input
         var cant = input.value.trim().length;
         //Elemento donde colocaremos la alerta
         var alerta = input.nextElementSibling;
         // Si tiene menos de 1 esta vacio
         if(cant < 1) {
         // Mensaje de alerta 
         alerta.innerHTML = 'Input Vacío';
         // Coloreamos de rojo las letras
         alerta.style.color = 'red';
         return false;
         // Si es mayor que el maximo permitido
         } else if(cant > max) {
         // Mensaje de alerta
         alerta.innerHTML = max + ' Máximo alcanzado, tienes ' + cant; 
         // Coloreamos de rojo las letras
         alerta.style.color = 'red';
         return false;
         // Si todo va bien con la cantidad de caracteres
         } else {
         // Mensaje de todo va bien
         alerta.innerHTML = cant + ' Caracteres escritos, máximo ' + max; 
         // Coloreamos de verde las letras
         alerta.style.color = 'green';
         return true;
         } 
      }); 
   </script> 
