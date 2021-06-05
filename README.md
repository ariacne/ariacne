-<!DOCTYPE html>
<html>
<body>

    <h1>Programa 4</h1>
    <h3>funciones</h3>
    <table border ="1"-cellspacing="0">
       <tr>
           <td>Nombre</td>
           <td><input type"text" id-"nombre" value=Martin></td>
       </tr>   
       <tr>
           <td>Apellido </td>
           <td><input type"text" id-"Apellido Paterno" value=Perez></td>
           </tr> 
            <tr>
            <td>Carrera</td>
            <td>
                <select id="Carrera">
                     <option value="">seleccione</option>
                    <option value "INID"select>ingenieria</option>
                    <option value "DER"select>derecho</option>
                    <option value "LAE"select>Administracion</option>
                </select>
            <td>
        </tr> 
        <tr>
             <td>Matricula</td> 
             <td><input type="number" id="matricula" value=""></td>
        </tr>
        <tr>
             <td>promedio</td>
              <td><input type="number" id="promedio" min="5" max="10"></td>
         </tr>
         <tr>
             <td colspan= "2" style="text-aling:center;">
             <input type="button" value="promedio" onclick =muestraboton()">
            <input type ="button" value="continuar" onclick="muestradatos()"> 
            <input type="button" value="limpiar" onclick="limpiar()">
         </td>       
      </tr>
  </table>
    <p id="resultado"> el resultado se mostrar aqui</p>
   <input type="button" id="boton" value="" style="">
</body>    
          
<script>          
     var nombre;
     var apellido;
     var carrera;
     var matricula;
     var promedio;
     var boton;
     var estiloexcelente='width:180px;height:180px;background-color:blue';
     var estilobueno='width:160px;height:160px; background-color:yellow';
     var estiloregular='width:140px;height:140px; background-color:green';
     var estilomalo='width:120px;height:120px; background-color:red';
     var estilopesimo='width:100px;height:100px; background-color:pink';
     var Resultado =document.getElementById("resultado");
     
     nombre=document.getElementById("nombre")
     apellido=document.getElementById("apellio")
     carrera=document.getElementById("carrera")
     matricula=document.getElementById("matricula")
     promedio=document.getElementById("promedio")
     boton=document.getElementById("boton")
     
 
 
     function muestra dato() 
     {resultado.innerHTML='hola mi nombre es'+ nombre.value +' '+ apellido.value + 'estudio la carrera con clave'+ carrera.value +' y mi matricula es'+ matricula.value;}
     
    
      function muestraboton()
      { 
      if (promedio.value>=10){
         boton.value="excelente";boton.style=estiloexcelente;
          }
         if(promedio.value>=9){
         boton.value="bueno";boton.style=estilobueno;
          }
       else
            if
           (promedio.value<=8){
            boton.value="regular";boton.style=estiloregular;
          }
        else
             if(promedio.value<7){
             boton.value="malo"; boton.style=estilomalo;
         }
         if(promedio.value<5){
           boton.value="pesimo";boton.style=estilopesimo;
          }
      }
      
     function limpiar()
     { 
     nombre.value='';
     apellido.value='';
     matricula.value='';
     
     }
     
</script>
       
</html>
