# MONDAY CHALLENGES

## "this" is a problem


![image](https://user-images.githubusercontent.com/117783981/214958041-fd6ff34c-32c4-43c6-b37b-07580348a7b0.png)

/* Al principio se estaba devolviendo un objeto {}, por lo cual se elimina y se reemplaza por la propiedad this.name en donde se almacena el first 
y last name
*/

function NameMe(first, last) {

    this.firstName = first;
    this.lastName = last;
    this.name = first + ' ' + last;
}


## Thinkful - List and Loop Drills: Lists of lists

![image](https://user-images.githubusercontent.com/117783981/214979692-1fd47c93-7f0a-4666-ae22-d83ce4e3e653.png)

function processData(data){
  
  let product = 1; // Se inicializa la variable a donde se va a almacenar el resultado de la suma 
      
  /*
  Se itera adentro del array anidado con data[i][0] donde el primer [i] se utiliza para iterar sobra el 
  indice "i" del array primario y el segundo [0] para iterar sobra la primera posicion del array interno
    
  */
  
    for (let i=0; i<data.length; i++) 
      {
        let res = data[i][0] - data[i][1];
        
        product = product * res;
        
      }
      
  return product;
  
}


## Stop gninnipS My sdroW!

![image](https://user-images.githubusercontent.com/117783981/214986994-eb7ffe77-4f38-42ec-9a1d-a6c0f27a1db3.png)


/*
Se requiere que si en un string unao mas palabras tiene 5 letras o mas, el string sea deuvelto
con esas palabras al reves.

Primero: Declaramos la const words y en esta se utiliza el metodo .spli(" ") para almacenar cada palabra por separado
Segundo: Iteramos sobre el array donde se almaceno cada palabra
Tercero: En la iteracion tenemos la condicional if donde verifica que si el length de la palabra es mayor a 5 haga lo siguiente:
  * Cada palabra (words[i]) la separa en sus letras usando .split("")
  * A las letras les cambia el orden .reverse()
  * Vuelve a unir las letras usando .join("")
Cada palabra la guarda en el array "words"

Por ultimo en el return utilizamos nuevamente join(" ") solo que el argumento es un espacio vacio, para que la frase sea retornada con 
sus espacios en blanco correspondientes y no todas las palabras juntas. El join(" ") tambien concatena las palabras de un array en un string.

*/


function spinWords(string) {

  const words = string.split(" ")
  
  for (let i = 0; i<words.length; i++) {
    if (words[i].length >= 5) {
      words[i] = words[i].split("").reverse().join("");
      
    }
     
  }
  
   return words.join(" ");  
}


