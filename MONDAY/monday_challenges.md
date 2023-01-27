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
