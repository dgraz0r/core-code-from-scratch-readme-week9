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
