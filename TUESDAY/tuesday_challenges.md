# TUESDAY CHALLENGES

## "this" is an other problem

![image](https://user-images.githubusercontent.com/117783981/215009432-7f87cb8f-0602-4ce4-ba0a-f764c1a46862.png)

function NamedOne(first, last) {

  this.firstName = first;
  this.lastName = last;

  Object.defineProperty(this, "fullName", {
    set: function(value) {
      var parts = value.split(" ");
      if (parts.length === 2) {
        this.firstName = parts[0];
        this.lastName = parts[1];
      }
    },
    get: function() {
      return this.firstName + ' ' + this.lastName;
    }
  });
  
}


## Who likes it?


![image](https://user-images.githubusercontent.com/117783981/215021840-bed7a8a3-bce5-4b4a-a56d-a5ce0c8db6ec.png)

*/
La funcion like recibe el parametro names que es un array.
Se utiliza switch para evaluar los casos presentados y se usa el la propiedad .length para definir que caso utlizar (cantidad de likes)
caso 0: no hay likes
caso 1: se utiliza un string literal y con ${} se introduce codigo donde names[0] indica la posicion 0 del arreglo
caso 2: se utiliza un string literal y con ${} se introduce codigo donde names.join(" and ") para unir los elementos dentro del array
caso 3: se utiliza un string literal y con ${} se introduce codigo donde ${names.slice(0, 2) retorna los valores del array contenidos
entre la posicion 0 y 2 y con .join(", ") los unimos con una coma, despues ${names[2]} devuelve el valor del array en la posicion 2
caso default: se utiliza un string literal y con ${} se introduce codigo donde ${names.slice(0, 2) retorna los valores del array contenidos
entre la posicion 0 y 2 y con .join(", ") los unimos con una coma, despues ${names[names.length - 2]} muestra la cantidad de items en el array 
menos 2

*/

function likes(names) {

   switch (names.length) {
    case 0:
      return "no one likes this";
    case 1:
      return `${names[0]} likes this`;
    case 2:
      return `${names.join(" and ")} like this`;
    case 3:
      return `${names.slice(0, 2).join(", ")} and ${names[2]} like this`;
    default:
      return `${names.slice(0, 2).join(", ")} and ${
        names.length - 2
      } others like this`;
  }
}
