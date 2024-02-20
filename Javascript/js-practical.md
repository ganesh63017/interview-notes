

# Javascript Coding Questions

1. **block scope:**

```js
{
const a=5; // or let a = 5;
}
console.log(a);

```
**#Output:**

```
ReferenceError: a is not defined

Note:use var for avoid error (var is hoisted)

```

---

2. **shadowing:**

```js

 function test(){
        const a = "Hello";   // or let a = "Hello";
        if(true){
            const a = "hi";
            console.log(a);   //or use let a = "hi";
        }
        console.log(a)
    }
    
    test();

```

**#Output:**

```
hi
Hello

```
---

3. **shadowing with let to var:**


```js
  function test(){
        var a = "Hello";   
        let b = "Bye";
        if(true){
            let a = "hi";
            var b= "Goodbye"  // error already taken
            console.log(a);
            console.log(b);
        }
    }

 test();
```

**#Output:**

```
Uncaught SyntaxError: Identifier 'b' has already been declared 

```
--- 


4. **shadowing with var:**
   
```js
  function test(){
         var a=10;
         var a=20;          
         console.log(a)
    }

 test();
```

**#Output:**

```
20

```

---


map:

  let arr = [1,2,3,4];
    
    let newArr = arr.map((num,i,arr) =>{
        return num * 10;
    
    })
    
    console.log(newArr)


    ** PolyFill for map **

    Array.prototype.myMap = function(cb){
        let temp = [];
        for(let i=0;i<this.length;i++){
            temp.push(cb(this.[i],i,this));
        }
        return temp;
    }

--------------------------------------

filter:


    
    let arr = [1,2,3,4];
    
    let newArr = arr.filter((num) =>{
        return num%2==0;
    
    })
    
    console.log(newArr)


    **PolyFill for Filter **

         Array.prototype.myFilter = function(cb){
        let temp = [];
        for(let i=0;i<this.length;i++){
           if(cb(this[i],i,this))  temp.push(this[i]);
        }
        return temp;
    }
--------------------------------------


reduce: 

    let arr = [1,2,3,4];
    
    let newArr = arr.reduce((acc,next,i,arr) => {
       return acc + next; 
    },0)
    
    console.log(newArr)

 ** PolyFill for Reduce **

  Array.prototype.myReduce = function(cb,initialValue){
       
        var accumulator = initialValue;
        for(let i=0;i<this.length;i++){
          accumulator = accumulator ? cb(accumulator,this[i],i,this) :
          this[i];
        }
        return accumulator;
    }

--------------------------------------



const arr = [2,5,9,11,44];


const mapResult = arr.map((ar)=>{
    return ar + 2;
})

console.log(mapResult); // ans -> [ 4, 7, 11, 13, 46 ]

const forEachResult = arr.forEach((ar,i)=>{
    arr[i] = ar + 3;
})

console.log(forEachResult); // and -> undefined

----------------------------------------------------------------------------

// Question: return total marks for students 
//with marks greater than 60 after 20 marks have been
//added to those who scored less than 60


let students = [
    
 {name:'abcd',rollNo:23,marks:90},
 {name:'xyz',rollNo:33,marks:70},
 {name:'pqr',rollNo:43,marks:30},
 {name:'lmn',rollNo:53,marks:63},
 {name:'mno',rollNo:63,marks:50},

 
]


  const data = students.map((stu)=>{
        if(stu.marks < 60){
            stu.marks += 20;
        }
        return stu;
    } ).filter((stu) => stu.marks > 60)
    .reduce((pre,stu) =>{
        return pre + stu.marks 
    },0)
    
  console.log(data)
----------------------------------------------------------------------------

    First Class Function:


    function square(num){
        return num * num;
    }


    function displaySquare(fn){
        
        console.log("Square is: "+ fn(5));
    }
    
    displaySquare(square);

----------------------------------------------------------------------------

  // What is IIFE (Immediatly Invoked Function Expression)
        
        ((num)=>{
            console.log(num * num);        
        })(5);

----------------------------------------------------------------------------

        ((num)=>{
            return (function(y){
                console.log(num);     // 1 
            })(10);
        })(5);
----------------------------------------------------------------------------
 for(var i=0;i<5;i++){
            setTimeout(() =>{
                console.log(i); // 5 5 5 5 5
            },i*1000)
        }



 -------------------------------------------------------

   
    function fun(x,y){ // parameter
        console.log(x*y);
    }
    
    fun(5,10)  // arguments
       
-------------------------------------------------------

    function fun(...nums){ // rest opeator
        console.log(nums);
    }
    
    let arr = [5,10];
    
    fun(...arr)    // spread operator

----------------------------------------------------------------

    callback function:

     function printOp(op){
        console.log(op);
    }
    
    function takeIp(fn){
        let greet = 'Hi Good Morning!!!';
        fn(greet);
    }
    
    takeIp(printOp);


----------------------------------------------------------------

Arrow Function:


  function fun(){   // with normal function we can check arguments also
      console.log(arguments); // use arguments its inbuild keyword
  }
  
  fun(1,2,3,4,5)



    fun = () =>  console.log(arguments); // using arrow function
  
  fun(1,2,3,4,5)  // error arguments is not defined



----------------------------------------------------------------------------

this:

    let user = {
        userName:"Admin",
        arrowFun:()=>{
            console.log("User Name: "+this.userName);  // this refers to globaly
        },
        regFun(){
                    console.log("User Name: "+this.userName); // this referes to user object
        }
        
    }
    
    user.arrowFun();
    user.regFun();

----------------------------------------------------------------------------

 // closure in js

    // closure scope chain

        function makeFun(){
            var name = "ABCD";
            function display(){
                console.log(name);

                function fun3(num){
                    console.log('this is fun 3, num= ',num);
                }
                return fun3;
            }

            return display;
        }

        makeFun()()(10);

----------------------------------------------------------------------------
    var e = 10;

            function sum(a){
                return function(b){
                    return function(c){
                        return function(d){
                            return a + b + c+d+e;
                        }
                    }
                }
            }

    console.log(sum(20)(30)(40)(50)); // 150

----------------------------------------------------------------------------
   let count =0;
        (function print(){
            if(count ===0){
                let count =1; // shadowing
                console.log(count); // 1
            }
            console.log(count); // 0
        })();
----------------------------------------------------------------------------

 // time optimization

        let a = [];

        function find(){
            for(let i=0;i<1000000;i++){
                a[i] = i * i;
            }

            return function(index){
        
              console.log(a[index]);
            }
        }

        const closure = find();

  

  console.time("6");
  // find(6);      // without time optimization

  closure(6);       // with time optimization

  console.timeEnd("6");

  console.time("12");
  // find(12);     // without time optimization

  closure(12);     // with time optimization

  console.timeEnd("12");

----------------------------------------------------------------------------


      for(var i=0;i<3;i++){
        setTimeout(function log(){
          console.log(i);   // if var : 3 3 3 
        },1000);            // if let : 0 1 2
       }
----------------------------------------------------------------------------

 // print 0 1 2 without using let use var only

  for (var i = 0; i < 3; i++) {
        function inner(i) {
          setTimeout(() => {
            console.log(i);
          }, 1000);
        }
        inner(i);
      }

----------------------------------------------------------------------------

Q: How would you use a closure to create a private
counter?

 function counter(){
        var _counter = 0;

        function add(increment){
          _counter += increment;
        }

        function getCounter(){
          return "Counter: "+ _counter;
        }

        return {
          add,
          getCounter
        }
       }

       const cnt= counter();

       cnt.add(10);
       cnt.add(20);
       console.log(cnt.getCounter());

----------------------------------------------------------------------------
// Q: What is Module Pattern ?

      var Module = (function(){
          function privateMethod(){
            console.log("Private");
          }

          return{
            publicMethod:function(){
              console.log('public');
              // privateMethod();
            }
          }
      })();

      Module.publicMethod();
      Module.privateMethod(); // cant access directly

----------------------------------------------------------------------------
// Make this run only once

      let view;
      function fun(){
          let cnt =0;
         return function one(){
          if(cnt === 0){
            view = "World!!!";
              console.log("Hello "+view);
              cnt++;
          }  

          } 


      }

    let one =fun();
    one();
    one();
    one();
 -----------------------------------------------


        // Once Polyfill:

        function once(func,context){
          let ran;

          return function(){
            if(func){
              ran = func.apply(context || this, arguments);
              func = null;
            }

            return ran;
          }
        }

    const hello = once(() => console.log("hello"));
    
    hello();
    hello();
    hello();
    hello();

 -----------------------------------------------

 // Q: Implement Caching/Memoize Function

         function myMemoize(fn,context){
            const res = {};
            return function(...args){
              var argsChache = JSON.stringify(args);
              
              if(!res[argsChache]){
                res[argsChache] = fn.call(context || this, ...args);

              }
              return res[argsChache];
            };

         }

         const fun = (num1,num2) =>{
          for(let i=0;i<= 10000000;i++){

          }

          return num1 * num2;
         }
     
         const memoizedFun = myMemoize(fun);



         console.time("First call");
          console.log(memoizedFun(1000,2000));
          // console.log(fun(1000,2000));

         console.timeEnd("First call")

         console.time("Second call");
          console.log(memoizedFun(4000,9000));

          // console.log(fun(1000,2000));
          console.timeEnd("Second call");


-----------------------------------------------
    // Difference between closure and scope

-----------------------------------------------


    Currying:

    function fun(num1){
          return (num2)=>{
              console.log(num1 * num2)
          }

      }

      fun(5)(10);

-----------------------------------------------



      function fun(type){
 
        return (no1)=>{
          return (no2)=>{
     
              if(type){
                if(type === "sum"){
                  return no1 + no2;
                }else if(type === "sub"){
                  return no1 - no2;
                }else if(type === "mult"){
                  return no1 * no2;
                }else if(type === "div"){
                  return no1/no2;
                }else{
                  return "Not correct type";
                }
              }     
                     
          }
        }
      }


    //  console.log( fun("mult")(10)(2));

        const mul = fun("mult");
        console.log(mul(10)(20));
        console.log(mul(30)(20));

-----------------------------------------------

    Infinite Currying:

      function add(a){
          return (b)=>{
            if(b) return add(a+b);
            return a;
          }
        }
      
       
      console.log(add(5)(2)(7)(8)(18)(10)(20)());

---------------------------------------------------

Currying VS Partial Application:

  
---------------------------------------------------

Manipulating DOM (use Currying):


<body>
 <h1 id="heading">Hello</h1>

    <script>
      function updateElementText(id){
        return function(content){
          document.querySelector("#" + id).textContent = content;
        }
      }
      
      const updateHeader = updateElementText("heading");

      updateHeader("Hi, Good Morning!!!");


    </script>

</body>

---------------------------------------------------

*** Curry() implementation:


 // curry() implementation
      // Converts f(a,b,c) into f(a)(b)(c)

      function curry(func){
        return function curriedFunc(...args){
            if(args.length >= func.length){
              return func(...args);
            }else{
              return function(...next){
                return curriedFunc(...args,...next);
              }
            }

        }
      }

      const sum = (a,b,c,d) => a + b + c + d;
      const totalSum = curry(sum);

      console.log(totalSum(1)(5)(6)(7))

---------------------------------------------------


    Objects in Javascript:

        const user = {
      name:"Abcd",
      age:29
     }

     user.name = "Ram";

    //  delete user.age 

     console.log(user)

-----------------------------------------------------------
 const fun = (function (a){
          delete a; // delete only object property not local variable
          return a;
      })(10);
 
      console.log(fun)

----------------------------------------------------

      const porperty = "firstName";
      const name = "RAM TM"; 
      
      const user ={
        [porperty]:name
      }

      console.log(user.firstName);

----------------------------------------------------

   const user ={
      name:'ABCD',
      age:20,
      sal:20000,
      status:'single'
     }

     for(key in user){
        console.log(key+" : "+user[key]);
     }

----------------------------------------------------

Check length of object:

Object.keys(objName).length

----------------------------------------------------


 const a = {};
      const b = {key:"b"};
      const c = {key:"c"};
     
      a[b] = 123;   // a["[object Object]"]  means "[object Object]" = 123
     
      a[c] = 456;  // a["[object Object]"] (overlap to) "[object Object]" = 456 


      // console.log(a[b]);

----------------------------------------------------

   console.log([..."abcdefghijklm"])

   it spread values and create an array
----------------------------------------------------

  let obj = {
          name:'abcd',
          age:30,
          no:101010101,
          address:'pune'
        }
        
        let admin = {
          ...obj,
          admin:true,
        }

        console.log(admin)

----------------------------------------------------
 
      const user ={
        name:'abcd',
        age:20,
        sal:30000
      }

      const data = JSON.stringify(user,["age","sal"]);

      console.log(data); // only age and sal will be strinify

----------------------------------------------------


   const shape = {
        radius:10,
        diameter(){
          return this.radius * 2; // reference to shape object
        },
        perimeter: ()=>  2 * Math.PI * this.radius // arrow fun refer to window object

      }

      console.log(shape.diameter());
      console.log(shape.perimeter())

----------------------------------------------------

        // what is destructuring in objects ?

      let user = {
        name:'ABCD',
        age:24,
        address:{
          street:'xyz road',
          city:'pune',
          pin:202020
        }
      };

      // const name = "XYZ" // if any other name is there

      // const {name:myName} = user;
      // console.log(myName);



      const { address: {city}} = user

      console.log(city)
----------------------------------------------------



  // function getItems(fruitList,...args,favFruit){   // error code line
      function getItems(fruitList,favFruit, ...args){ // ...args is the rest parameter must be last as parameter
        return [...fruitList,...args,favFruit];  // this ...args is spread operator
      }

     console.log( getItems(["banana","apple"],"pear","orange"));
----------------------------------------------------
    
    // Object reference

  let c = {geeting:"hi"};
     let d;

     d = c;

     c.geeting = "hello";

     console.log(d.geeting)

---------------------------------------------------------------
        
        console.log({a:1} == {a:1});   // false
        console.log({a:1} === {a:1});  // false

----------------------------------------------------------------

 let person = {name:"ram"};
      const members = [person];
      person= null;
      
      console.log(members) // array with 0th position person obj
----------------------------------------------------------------


      let person = {name:"ram"};
      const members = [person];
      // person= null;
      
      // console.log(members) // array with 0th position person obj

      person.name = null;

      console.log(members) // name : null -> impacted
----------------------------------------------------------------

 
        const value = {number:10};

        const multiply = (x = {...value}) => {  // ...value --> its clone of object value
          console.log(x.number *= 2);
        }

        multiply();  // 20
        multiply();  // 20
        multiply(value); // 20  // passing actual obj ref and it will copied into x and then it will change value of x = 10 to x =20 
        multiply(value);  //40

----------------------------------------------------------------

   function fun(obj1){
        obj1.age = 25;

        obj1 = {
          name:'John',
          age:50
        }

        return obj1;

      }

      const obj1 = {
        name:'Alex',
        age:30
      }

      const obj2= fun(obj1);

      console.log(obj1); //{name: 'Alex', age: 25}
      console.log(obj2); // {name: 'John', age: 50}

----------------------------------------------------------------


      // What's shallow Copy and Deep Copy ?

      // shallow Copy : one obj hold the reference of another obj


     /* 
      let obj = {
        name:'ram',
        age:20
      }

      newObj = obj;
      
      newObj.age = 50;

     
      console.log("Old Obj: "+ obj.age +"\nNew Obj: "+ newObj.age); // both age = 50 
      */
      
      
      // Deep Copy: one obj cloned with another obj variable
      
      let obj = {
        name:'ram',
        age:20
      }

      // let newObj = {...obj};  // (destructuring) copy obj to newObj & not ref

      // let newObj = Object.assign({},obj); // 2nd way
      
      // let newObj = JSON.parse(JSON.stringify(obj)); // 3rd way

      newObj.age = 55;
      
      console.log(newObj.age);    // 55   
      console.log(obj.age);  // 20


----------------------------------------------------------------

//********** This keyword **********

     // implicit binding & explicit binding

     // implicit binding usually this keyword use with . operator

     // explicit binding includes call, bind, apply 


        //   a = 10;   // for var and only a show op but let & const not shows
        // console.log(this.a) // 10 

----------------------------------------------------------------
  
      a = 10;

     function fun(){
      console.log(this.a); // var a & only a works but 
     }                      // let and const not works because its not global

     fun();

----------------------------------------------

 this.a = 5;

      const fun = () =>{
        console.log(this.a);  // same as above eg
      }

      fun();
----------------------------------------------

 this with normal function VS arrow Function:


  ***using  normal function ***


    // let data  = {
    //   name:"abcd",
    //   age: 30,
    //   getData(){
    //     console.log(this.name);
    //   }
    // }

    // data.getData();

    

    // let data  = {
    //   name:"abcd",
    //   age: 30,
    //   childObj:{
    //     newName: "ram",
    //     getData(){
    //       console.log("Child: ",this.newName,"\nParent: ",this.name);
    //     }

    //   }


    // }

    // data.childObj.getData(); // ram undefined


----------------------------------------------

  ***using  arrow function ***



 // let data  = {
    //   name:"abcd",
    //   age: 30,
    //   getData: ()=> {
    //       console.log(this) // undefined its pointing to window obj

    //       // arrow function take reference from its parent function
    //       // and parent function must be normal function ow its refer to window
      
    //     }


    // }

    // data.getData(); 
      


    let data  = {
      name:"abcd",
      age: 30,
      getData(){
          const nestedArrow = () => {
            console.log(this.name);
          }     
          nestedArrow(); 
        }


    }

    data.getData(); 

--------------------------------------------------------------------------------------------

        class user {
        constructor(n){
          this.name = n;
        }

   
        
        getName(){
          console.log(this.name)
        }
     
      }

      let obj = new user('ram');

      obj.getName();

--------------------------------------------------------------------------------------------

  const user = {
      firstName:'ram',
      getName(){
        const firstName = "Virat";
        return this.firstName;
      }
    }

    console.log(user.getName()); // ram



--------------------------------------------------------------------------------------------


      function makeUser(){
        return {
          name:'Ram',
          ref:this,
   
          
        }
      }

      let user = makeUser(); // pointing to parent obj which is window obj

      console.log(user.ref.name);

--------------------------------------------------------------------------------------------
 
 for fix above problem:

  function makeUser(){
        return {
          name:'Ram',
         ref(){
          return this;
         }
   
          
        }
      }

      let user = makeUser(); 

      console.log(user.ref().name);

--------------------------------------------------------------------------------------------



  const user = {
      name:"ram",
      logMsg(){
        console.log(this.name); 
      }
     }

// setTimeout(user.logMsg,1000); // prints undefine or nothing
 
setTimeout(()=>{  // to solve problem call method in func
  user.logMsg();
},1000);


--------------------------------------------------------------------------------------------
     const user = {
        name:"ram",
        greet(){
          return `Hello ${this.name}`
        },

        farewell:()=>{
          return `Goodbye, ${this.name}`

        }
        
      }

      console.log(user.greet()); // Hello ram
      console.log(user.farewell()); // Goodbye undefined or null

      // to solve problem make farewell normal function or put in normal function


--------------------------------------------------------------------------------------------


   let calculator = {
            read(){
              this.a = +prompt("a = ",0);
              this.b = +prompt("b = ",0);

              
            },
            sum(){
              return this.a + this.b; 
            },
            mul(){
              return this.a * this.b;
            }
        }

        calculator.read();
        console.log(calculator.sum());
        console.log(calculator.mul());

// work without this also throughout program

--------------------------------------------------------------------------------------------

        var length = 4;

        function callback(){
          console.log(this.length);
        }

        const object = {
          length:5,
          method(fn){
            fn();
          }
        }

        object.method(callback); // 4
--------------------------------------------------------------------------------------------
    var length = 4;

        function callback(){
          console.log(this.length); // length of array 3
        }

        const object = {
          length:5,
          method(){        // arguments = [callback,2,3]
            arguments[0]();
          }
        }

        object.method(callback,2,3);

--------------------------------------------------------------------------------------------
   
   let calc = {
        total: 0,
        add(no){
          this.total += no;
          return this
        },
        mult(no){
          this.total *= no;
          return this

        },
        sub(no){
          this.total -= no;
          return this

        }    
        
      }

      
      const result = calc.add(10).mult(5).sub(30).add(10);
      console.log(result.total);
--------------------------------------------------------------------------------------------

**** Explicit binding (call,apply,bind) *****


call:
      var obj = {name:'ABCD'};

        function sayHello(){
          return "Hi" + this.name
        }

        console.log(sayHello());  // only Hi prints 


------------------------------------------------------------

    var obj = {name:'ABCD'};

        function sayHello(age,add){
          return "Hi, My name is " + this.name  + " I am " + age + " old"
        }

        console.log(sayHello.call(obj,30,'pune'));


------------------------------------------------------------

apply:


        var obj = {name:'ABCD'};

        function sayHello(age,add){
          return "Hi, My name is " + this.name  + " I am " + age + " old"
        }

        console.log(sayHello.apply([obj,30,'pune']));
------------------------------------------------------------

bind:

    var obj = {name:'ABCD'};

        function sayHello(age){
          return "Hi, My name is " + this.name  + " I am " + age + " old"
        }

        const bindFun = sayHello.bind(obj);
        console.log(bindFun(30));

------------------------------------------------------------

// find the op:


  const person = {name:'ram'};

    function fun(age){
      return `name is ${this.name} & age is ${age}`;
    }

    console.log(fun.call(person,23));
    //console.log(fun.apply(person,[23]));
    console.log(fun.bind(person,23));


------------------------------------------------------------

 const age = 10;

        var person = {
          name:"ram",
          age:20,
          getAge:function () {
            return this.age;
          }
        }

        var person2 = {age:24};
       console.log( person.getAge.call(person2)); // 24

------------------------------------------------------------



      var status = 'a';


      setTimeout(()=>{
            const status = 'b';
           const data = {
            status:'c', 
            getStatus(){
                return this.status;
             }

           };

           console.log(data.getStatus()); // c
           console.log(data.getStatus.call(this)); // a


      },0)

------------------------------------------------------------

       const animals =[
          {species:"lion",name:"king"},
          {species:"whale",name:"Queen"},

        ]

        function printAnimals(i){
          this.print = function(){
            console.log("#"+i+" "+this.species+": "+this.name);
          };
          this.print();
        }

        for(let i=0;i<animals.length;i++){
          printAnimals.call(animals[i],i);
        }
------------------------------------------------------------




  const arr = ["a","b"];
  const ele = [0,1,2];

 
   arr.push.apply(arr,ele);

   console.log(arr);
     
------------------------------------------------------------

        const num = [5,9,2,17,1];
        console.log(Math.max.apply(null,num))
        console.log(Math.min.apply(null,num))

------------------------------------------------------------
  function f(){
          console.log(this); // 
        }

        let user = {
          g: f.bind(null)
        }
       
        user.g(); // pointing to window object
------------------------------------------------------------

 function f(){
          console.log(this.name);
        }

        f = f.bind({name:"ABCD"}).bind({name:"XYZ"}); // bind chaining not working only once it will bind with object

        f();

------------------------------------------------------------


function checkPassword(success,failed){
        let password = prompt("Password?","");
        if(password == "ABCD") success();
        else failed();
       }

       let user = {
        name:"RAM",
        loginSuccess(){
          console.log(`${this.name} logged in`);
        },
        loginFailed(){
          console.log(`${this.name} failed to log in`);
        }
       }

       checkPassword(user.loginSuccess.bind(user),user.loginFailed(user));


------------------------------------------------------------



  
 **** javascript coding quetion ************

callback method

--------------------------------------------------------------------
 1. how to define a class with properties and methods in js
--------------------------------------------------------------------
               class car{
            constructor(model,name){
               this.model = model;
               this.name = name;
            }
            
            start(){
               console.log(`car name is ${this.name}`);
            }
         }

         bmw = new car('2016','BMW');

         bmw.start();


--------------------------------------------------------------------
 2. how to implement class inheritance in js?
--------------------------------------------------------------------


class Car{
    constructor(model,name){
        this.model = model;
        this.name = name;
    }
    
    start(){
        console.log(`car name is: ${this.name}`);
    }
}

class BMW extends Car{
    dashboard(){
        console.log('child function');
    }
    call(){
        super.start();
        this.dashboard();
    }
}

bmw = new BMW('bmw2016','BMW');

bmw.call();


--------------------------------------------------------------------
   3. how to find duplicate elements in given array ?
--------------------------------------------------------------------
  
    const arr = [10,20,30,40,20,60,70,10];
    
    const duplicate = arr.filter((el,index,array) => arr.indexOf(el) !== index );
    
    console.log(duplicate);



     //const arr = [10,30,10,40,20,10];
    
    // const unique = arr.filter((el,index,arr) => arr.indexOf(el) == index)
    
    // console.log(unique);
  

--------------------------------------------------------------------
   4. How to find the count of duplicates in an array?
--------------------------------------------------------------------
  
    const arr = [10,20,30,40,20,60,70,10,90,20];
    
const count = arr.reduce((obj,el) => {
    if(obj[el] == undefined){
        obj[el] =1;
        return obj;
    }else{
        obj[el]++;
        return obj;
    }
},{});

console.log(count);
  
  
--------------------------------------------------------------------
  5. how to check if a given number is an integer ?
--------------------------------------------------------------------
    const no = 1;
    
    console.log(!isNaN(no));
    // Number.isInteger(no)
  

--------------------------------------------------------------------
  6. explain the difference between Object.freeze() vs const ?
--------------------------------------------------------------------

const month = 'July';

month = 'feb';

console.log(month);  // it will give an error



let person = {
   name:'abcd'
}

Object.freeze(person);

person.name = 'xzy';

console.log(person.name); 
// op: abcd not xyz, and no shows any error if not in strict model
// but in strict mode it will also give an error (cannto assign value to readonly property)



--------------------------------------------------------------------
  7. how to sort a number array?
--------------------------------------------------------------------

  const arr = [40,20,80,20,10,80,100];
    
    const sorted = arr.sort((a,b)=>{
        return a - b;
    });
    
    console.log(sorted)  
  
--------------------------------------------------------------------
  8. how to sort given string array ?
--------------------------------------------------------------------
 
 const arr = ['jan','feb','march','aug','may'];   
    
    console.log(arr.sort())
  
  
--------------------------------------------------------------------
  9. how to find unique values in an array?
--------------------------------------------------------------------
 
   const arr = [10,30,10,40,20,10];
    
    // const unique = arr.filter((el,index,arr) => arr.indexOf(el) == index)
    
    // console.log(unique);
  

    const unique = Array.from(new Set(arr)) // easy way
    
    console.log(unique)
  
  
--------------------------------------------------------------------
  10. How to find unique values from an array sorted order ?  
--------------------------------------------------------------------
 
    let arr = [20,40,20,50,60,70,10,50];
    
    let sorted = arr.filter((el,index,arr) => arr.indexOf(el) === index)
   .sort((a,b)=>{
        return a - b;
    } )
    
    console.log(sorted);
  
  
--------------------------------------------------------------------
  11. How to find maximum value in a numbered array ?
--------------------------------------------------------------------

  let arr = [20,40,20,50,60,70,10,50];
    
    let max = arr.reduce((pre,next) => {
        return pre > next ? pre : next;
    })
    
    console.log(max);
  
  
--------------------------------------------------------------------
  12. How to find minimum value in a numbered array ?
--------------------------------------------------------------------

  let arr = [20,40,20,50,60,70,10,50];
    
    let min = arr.reduce((pre,next) => {
        return pre < next ? pre : next;
    })
    
    console.log(min);

  
--------------------------------------------------------------------
  13. How to find the average of the numbers in the numbered array ?/
--------------------------------------------------------------------

    let arr = [10,20,40,0,80,30,40];
    
    let total = arr.reduce( (pre,next) => pre +  next,0)
    
    
    console.log(total/arr.length)
  
  
  
--------------------------------------------------------------------
  14.  how can you uppercase the first character in string array ?
--------------------------------------------------------------------

 
   const days = ['sun','mon','tue','wed','thu','fri','sat'];
  let newDay = [];
  days.forEach( (el) => {
    el = el.charAt(0).toUpperCase() + el.substring(1);
//   console.log(el)
    newDay.push(el);
  } )
  
  console.log(newDay)
  
  
--------------------------------------------------------------------
  15. How to make sentence out of a given array?
--------------------------------------------------------------------

    let arr = ['Welcome','to','Computer','World','!!!'];

// let sen ='';
// arr.forEach((el) =>{
//     sen += el + ' ';
// })

let sen = arr.join(" ");


console.log(sen);

  
--------------------------------------------------------------------
  16. How to check if an array contains any element of another array?
--------------------------------------------------------------------

  
  
  let arr1 = [1,2,3,4,5,6,7,8,9,10];

  let arr2 = [12];

  let ans = arr1.some( el => arr2.includes(el))

  console.log(ans)
  
  
--------------------------------------------------------------------
  17. Given two strings how can you check if the strings are anagram 
  for each other ?
--------------------------------------------------------------------

  
   let str1 = 'abc';
    let str2 = 'cbd';
    
    function checkAnagram(s1,s2){
    let a = str1.toLowerCase();
    let b=str2.toLowerCase();
    
    a=a.split("").sort().join("");
    b=b.split("").sort().join("");
    
    return a===b;
    }
    
    console.log(checkAnagram(str1,str2));
  
  
  
--------------------------------------------------------------------
  18. How can you extract a few fields from the given JSON object
  and form a new array ?
--------------------------------------------------------------------


    const data = {
    "emp": [
      {
        name:'abcd',
        id:101,
        sal:1000
      },
       {
        name:'xyz',
        id:102,
        sal:2000
      },
       {
        name:'pqrs',
        id:103,
        sal:3000
      },
       {
        name:'lmno',
        id:104,
        sal:4000
      }
    ]
  }
  
let result = data.emp.map((el) =>{
    // return el.name
    
    let newData = {
        name:el.name,
        sal:el.sal + 500
    }
    
    return newData
    
});

console.log(result)


--------------------------------------------------------------------
  String Questions: 
--------------------------------------------------------------------
    1. How do you check whether a string contains a substring?

      --> using includes (ES6):

      let str = 'hello';
      let substr='ell';

      console.log(str.includes(substr))
  
  
       --> using indexOf (ES5):

            let str = 'hello';
            let substr='ell';

            console.log(str.indexOf(substr) !== -1)
  

      --> using regex


*************************************


// explicit binding with arrow function


        const age = 10;

          var person = {
            name:"ram",
            age:20,
            getAgeArrow:() => console.log(this.age),
            getAge:function(){
              console.log(this.age)
            }
          }
          var person2 = {age:24};

          person.getAgeArrow.call(person2);
          person.getAge.call(person2);
          