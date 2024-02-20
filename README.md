# interview-notes
Interview prep notes for angular, typescript, js, hmtl, css and other



---

  ********* HTML & CSS  ************
 
CSS - position, display, margin
How to select multiple data from drop-down
what are html selectors
what are css selectors
why custom css - sass used

Scenario 1:- You have a dropdown in that you have options of cities. If you click on the city you would get the data as name and category. So how would you display the data in of the categories and name in a card.
 
 ********* JavaScript ************
 
 
 what are javascript data types  
 difference between let and const  
 let, var, const and can you write down some examples ? 
 Difference between map and filter.
 call apply bind js functions
map filter find - array methods
 prime number program
splice method
how to show reverse order in js? like 12345 - 54321 & also can show in typescript ?
 If we make 10 ajax requests, then how to catch it in one shot?
 difference between promise and observable ?  
 which is best promise or observable ?
 Various ways to create object in JS
 What is object literal in JS?
 How to use OOP in JS 
 What are classes in JS?
 what is singleton class
 How to implement singleton class?
 What is object oriented concepts used in javascript
 What is encapsulation , how to implement in javascript
 what is inheritance  , how to implement in javascript   
What is closure
hoisting?
Features of ES6 and what is ES6


What is RxJs
What is rxjs, useful methods from rxjs 
What concepts you used in rxjs
Operators of RxJS




 
 ********* Angular ************
 
Difference between Framework & library
What are your favorite libraries in Angular & why
Is Angular framework or library explain in detail
What is Angular
What is SPA
What are Building blocks of angular
What are Component
What is Template
 Explain latest features of the angular version you are working on ?
 difference between angular 8 and 9?
 Whole structure of angular?
 What is the difference between the Component and a directive?
event emiiter
decorator
custom pipe
What is async pipe
What directives and pipes
how to create dynamic component
Which form you use template driven or reactive forms
How to use shareable component
What is @INPUT & @OUTPUT decorators?
What is pipe? How to implement it?
What are validators in Angular? How to implement it?
 How would you validate a form in angular?
  How would you display the data in the frontend in angular?
  life cycle hooks
  What is directive? Types and syntax for ngif and ngfor
  Had you created a custom directive? had you created a directive in the project that you had done before?
how to share the data between two component? or How we can communicate across(pass data from one component to another) the components? 
What is routing?
wild card route
What is router-outlet
How to protect the routes?
What is lazy Loading ? how to implement?, advantages and disadvantage?
How to stop initial navigation until some condition is satisfied?
 what are services? why it had introduced in angular?
 how to create a service ?
dependency injection and why we used?
As we can also import the services in the components directly by creating the object of that services. So why we are using the dependency injection?
communication between modules?
 how to share data between two modules in angular ? 
How to show grid in angular? And how to show data in grid?
 how to use validation in search bar?
Types of event handler
How to handle error in angular? Syntax
If we want to search any data after entering 3 character How to implement that? 
 How would you get the data from the api in angular?
Explain different types of event in angular?
If you have a huge data then how would you show in the frontend in angular?
How would you implement sorting and filtering if you have got a huge amount of data in your table or grid.
what is main.js polyfill.js vendor.js
what is -o in command ng s -o?
what is single sign on? sso?
how to create JWT token?
session storage VS local Storage?
I have one lack recode in our application, how to show in web page ?
Difference between JIT & AOT
Benefits of trackBy
What is a Change Detection Strategy?
How to manage state in Angular => ngrx
How to make http calls
Explain build process of angular application
Difference between Subject & Behavior subject
What is View encapsulation in Angular
How to manage/handle session in ng
What is package.json & its need?
what are shared modules
what is http interceptor
What is authguard
callback promises observable
subject vs behaviouralSubject
app module - how to get other than app component as a home component
dependency and dev dependency - diff
change detection strategy
interceptor why used?
infinite scrolling npm pacakage
What are HTTPIntercepters?


 
----------Practical/Scenario questions-------------

create two different modules and components inside them. communicate in between with the help of subject.

Scenario: In a project, If you have three modules:- AppModule,ModuleA,ModuleB. and If you run the application the AppModule would be loaded and if i go to Module A, the module A would be loaded. After that i clear the cache memory and reload the application. Then if go directly on ModuleB. It would load moduleA and ModuleB. So what would be the mistake that had might done by the developer.


Scenario: 3api call- if get response from all , then only page should be load


 


****************Git/GitHub***********************

have you worked on Git or Git hub?
difference between pull and push ?
Now am in B1 branch, I need to change B2 branch, how to change and with commit or without commit the code ?
I did some changes in my code, so need to change another branch without commit, how will you able to do ?


****************** Non-Technical ****************************

asked that have you ever worked on project from scratch
intro about projects you have worked on




************************************************************


*** RoadsideCoder ***

imp to check:

1. implicit and explicit binding (apply, this,call,bind);
2. functions are first class object in js 
____________________________________________________________

block scope:

{
const a=5; // let a = 5;

}

console.log(a);


------------------------------------

shadowing:

  function test(){
        const a = "Hello";   // let
        if(true){
            const a = "hi";
            console.log(a);   //let
        }
        console.log(a)
    }
    
    test();


------------------------------------

shadowing with let to var:

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
--------------------------------------

         var a=10;
         var a=20;          
         console.log(a)



--------------------------------------


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



1. what the use of angular?

-> angular is js ui binding framework which binds html ui and js model (view modal)

mvvm / mvc / mvvm

adding to it, it is also helps you to build SPA (Single page application) by
 using concept of routing it also has lot of other features like 
 HTTP, DI, Input output bcoz of which you do not need other frameworks
 
 
 --------------------------------------
 
 2. diff betn angularjs vs angular
 
 ---------------------------------------
 
 3. what are directives in Angular ?
 
 --> Directives changes the behavior of HTML DOM
 
 e.g. ngModel, [hidden], {{anything}}

 
 ------------------------------------------------
 
 4. explain the different types of Angular Directives ?
 
 --> 3 types SAC (S: Structural, A: Attribute, C: component)
 
 1. Structural Directive: change the DOM layout by adding and removing elements.
 
	e.g *ngFor
	

 2. Attribute Directive: change the appearance and behaviour of HTML elements
 
 	e.g [hidden] , [disable]
 	
 3. Component Directive: Directives with templates. Its like a user control
 	
 
 ----------------------------------------------------------------------
 
 5. Explain the importance of NPM and node_modules folder?
 
 
 --> npm is package manager which makes installation of js framework easy.
 
 node_modules is the folder where all packages are installed.
 
 
 -------------------------------------------------------------------------
 
 6. explain the importance of package.json file in angular ?
 	
 	it has all the js references needed for a project, so rather 
 	than installing one package at a time we can install all 
 	packages in one go
 	
 ----------------------------------------------------------------------
 
 7. what is typescript and why do we need it?
 
 --> 	typescript superset of js, it added types to js
 
 	it gives a nice Object-Oriented programming environment
 	which transpiles / converts to js
 	
 	
 	so as its strongly types we will have less errors and bcoz 
 	we can do OOP with js our productivity and quality also 
 	increases
 	
 ------------------------------------------------------------------------
  
 8. explain importance of angular CLI ?
 
 -->  angular CLI is command line interface, by which we can create
       initial angular project template. So rather than starting
       from scratch we have some boiler plate code.
       
  -------------------------------------------------------------
  
  9. Explain the importance of Component and modules ?
  
  -->   component is where you write your binding code, 
  	 module logically groups components.
 	
 	
 	view -- > component <-- modal
 	              |		
 		     css 
 
 
 --------------------------------------------------------
 
 10. what is a decorator in Angular?
 
 -->  Decorator defines what kind of Angular class is it,
 	for example if you decorate @Component then it says it's
 	an angular component if you put @NgModule it becomes a 		Angular module
 	
  --------------------------------------------------------
  
  11. what are annotations or metaData ?
  
  --> same answer as decorator
  
--------------------------------------------------------
   
   12. what is a template ?
   
   --> template is an HTML view of Angular in which we can write 
   	directives. 
   	
   	there are two ways of defining template one is inline and 
   	other is a separate HTML file
 
   --------------------------------------------------------
   
   13. explain the four types of Data bindings in Angular?
   
--> data binds means how view (html) and component communicate with each other
 
       1) interpolation / expression binding --> {{}}
       : data flows from component to the view and we can mix
          the same with HTML tags.
       	   
       2) property binding --> []
       : data flows from component to view
       
       3) event binding --> click, keypress, keyup --> ()
       : when you want to send event from the view to component
       
       4) two way binding --> [()] 
 	:Data flows from component to the view and vice versa.
 
   --------------------------------------------------------
   
   14. explain the architecture of Angular ?
   
  -->  			        _____ a group of component present in module
  			()		|
  	  view      <-------->    Controller
  	    		[]	
  	(template)		   (Component)
  
  
  Points should be discuss: 
  
  1. Template : HTML view of Angular
  2. Component : Binds the view and Model
  3. Modules : Groups components logically
  4. Binding : Defines how view and component communicate
  5. Directives : changes the HTML DOM behaviour
  6. Service : Helps to share common logic across the project
  7. DI (Dependancy Injector) : it helps to inject instance across constructor
  
 
 --------------------------------------------------------
    
  15. what is SPA in Angular ?
    	
 --> Single page application
 
 	in this applications where the main UI gets loaded once,
 	and then the needed UI is loaded on demand  
    	
    	- performance improvement
    	
    -------------------------------------------------------- 
 16 :- How to implement SPA in Angular ?
 	
 --> in angular we use routing...
 
  
 
  --------------------------------------------------------
 17 :- How to implement routing in Angular ?
 
 -->     routing is a simple collection which has two things URL
      and when this URL is called which component to load.
      
      so routing helps you to define the navigation for your 
      angular application. so if you want to move from one 
      screen to other screen and you want to respect SPA 
      that means not loading and refreshing the whole UI
      routing is needed.
      
 
 

 
  --------------------------------------------------------
 18 :- Explain Lazy Loading ? 
 
 -->  it means on demand loading, loading only the 
     necessary HTML, CSS and js files so that you 
     have better performance.
     
  --------------------------------------------------------
 19 :- How to implement Lazy Loading in Angular ?
 
 --> divide your project in to modules
 
 	use "loadChildren to load module"
 
 
  --------------------------------------------------------
 20 :- Define Services ?
 
 -->  services helps you to share common logic across angular projects
 
 
  --------------------------------------------------------
 21 :- What is Depedency Injection ?
 
 -->	DI is an application design pattern where rather than
 	creating object instances from within the component
 	angular injects it via the constructor.
 
 
  --------------------------------------------------------
 22:- How to implement Depedency Injection ?
 
 --> use provider (in app module)
 
  --------------------------------------------------------
 23 :- Whats the benefit of Depedency Injection ?
 
 -->	DI helps to decouple class dependencies,
 	so that when you add new dependencies you do not have
 	change everywhere.
 
 	
 	if we create object in every component without using DI
 	then its becomes tightly coupled and if new changes 
 	occure then have to change everywhere
 
 
  --------------------------------------------------------
 24 :- Differentiate between ng Serve and ng build ?
 
 -->  "ng serve" builds in memory while,
 	
	"ng build" builds on the hard disk. 
	
	so when you want to go for production "ng build" 
	command is used.
 	
 
 
  --------------------------------------------------------
 25 :- Explain the --prod parameter in ng build ?
  
  -->  ng build --prod flag compresses your JS file, removes 
  	comments, creates GUIDs of your JS files and make
  	your application ready for production 
  
   --------------------------------------------------------
  
  *** ARC ***
  
  

  in component ts file --> 
  
  html: templateUrl has most preference than template,
        if we try to use both then templateUrl (external html file) has more preference.

   css: in styleUrls we can add external css file (other component css file) also. (in array)
   
   styleUrls and styles have same preference, but if we apply common properties then it will apply only from 
   styles and not from styleUrls.
   

  
  
  
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












 

