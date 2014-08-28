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
    


//Building a Cash Register
var cashRegister = {
    total:0,
    //Dont forget to add your property
    add: function(itemCost) {
        this.total +=  itemCost;
    },
    scan: function(item,quantity) {
        switch (item) {
        case "eggs": this.add(0.98 * quantity); break;
        case "milk": this.add(1.23 * quantity); break;
        case "magazine": this.add(4.99 * quantity); break;
        case "chocolate": this.add(0.45 * quantity); break;
        }
        return true;
    },
    //Add the voidLastTransaction Method here
    
    
};

cashRegister.scan('eggs',1);
cashRegister.scan('milk',1);
cashRegister.scan('magazine',1);
cashRegister.scan('chocolate',4);

//Void the last transaction and then add 3 instead


//Show the total bill
console.log('Your bill is '+cashRegister.total);
