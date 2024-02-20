
# Angular interview questions:


 difference between promise and observable ?  
 which is best promise or observable ?

 What is RxJs
What is rxjs, useful methods from rxjs 
What concepts you used in rxjs
Operators of RxJS



Difference between Framework & library
What are your favorite libraries in Angular & why
Is Angular framework or library explain in detail
What is Angular
What is SPA
What are Building blocks of angular
What are Component
What is Template
Explain latest features of the angular version you are working on ?
Difference between angular 8 and 9?
Whole structure of angular?
What is the difference bektween the Component and a directive?
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
Life cycle hooks
What is directive? Types and syntax for ngif and ngfor

Had you created a custom directive? had you created a directive in the project that you had done before?

How to share the data between two component? or How we can communicate across(pass data from one component to another) the components? 

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
How to use validation in search bar?
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

session storage VS local Storage?
I have one lack recode in our application, how to show in web page ?

Difference between JIT & AOT
Benefits of trackBy
What is a Change Detection Strategy?
How to manage state in Angular => ngrx
How to make http calls
Explain build process of angular application

Difference between Subject & Behavior subject & ReplaySubject & AsyncSubject (https://medium.com/@jaydeepvpatil225/observables-and-subjects-in-angular-a4d73dfa5bb)


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



-----------------------




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