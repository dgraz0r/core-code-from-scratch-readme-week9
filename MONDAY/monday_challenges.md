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
