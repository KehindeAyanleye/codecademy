Codecademy
==========
// Private Variables
function Person(first,last,age) {
   this.firstname = first;
   this.lastname = last;
   this.age = age;
   var bankBalance = 7500;
}

// create your Person 
var john = new Person("rg", "gr", 76);

// try to print his bankBalance
console.log(john.bankBalance);

//Instead, Accessing Private Variables
//By adding a method here: this.getBalance = function(){};


// Accessing Private Variables
function Person(first,last,age) {
   this.firstname = first;
   this.lastname = last;
   this.age = age;
   var bankBalance = 7500;
   
   this.getBalance = function(){
       return bankBalance;
       };
    }
    
    var john = new Person('John','Smith',30);
    console.log(john.bankBalance);
    
//create a new variable myBalance that calls getBalance()
    var myBalance = john.getBalance();
    console.log(myBalance);
