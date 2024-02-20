# Questions Lists:

## Angular:


    Advance:

    How to stop initial navigation until some condition is satisfied?

    Q. web accessibility
    Q. Angular upgrade
    Q. Explain angular deployment, how is it done?
   
    Q. Multilanguage support?	
    Q. What is responsive design? what is mobile-first approach?
    Q. How is angular app deployed?
    Performance optimization? (Using AoT Compilation, Using OnPush Change Detection Strategy, Using Pure Pipes, Unsubscribe from Observables,
    Lazy Loading, Use trackBy option for For Loop, Avoid computation in template files, Usage of Web Workers )
    
    Transpiling?
    
    
    How to easily make all properties of an interface optional? (const emp: Partial<Employee> = {};)
    
    Q. what are different ways to optimize a given project to minimize the rendering load and package size?? anything related to ng build? 
    (Ans: ng build with aot option, instead of default JIT compilation)

    app module - how to get other than app component as a home component
    
    
    dependency and dev dependency - diff
    
    "dependencies" : Packages required by your application in production. "devDependencies" : Packages that are only needed for local development and testing.
    
    
    

    infinite scrolling npm pacakage (to handle huge amount of data)
   
    what is single sign on? sso?
    how to create JWT token?
    session storage VS local Storage?

    Benefits of trackBy
    What is View encapsulation in Angular
    
    (View encapsulation defines whether the template and styles defined within the component can affect the whole application or vice versa)
    	Emulated (default) {styles==> main HTML to comp} ,  ShadowDom {not main HTMl to comp}, none {comp to main HTML}
    	
    
    How to manage/handle session in ng
    
    
    
     Change detection &   strategy  (imp) (https://www.xenonstack.com/blog/performance-optimization-in-angular)
    
    ******************************************
    Baiscs:

    What is SPA
    What is Angular
    Is Angular framework or library
    What are your favorite libraries in Angular & why
    Difference between Framework & library
    What are Building blocks of angular
    What is package.json & its need?
    What is @INPUT & @OUTPUT?
    What is input output decorators
    Promise ,Subscription
    how to create dynamic component
    How to use shareable component
    What is pipe? How to implement it?
    what is subject, behaviorsubject
    Inter component communication?
    cross component communication
    dependency injection
    Subject, Behaviour subject ,actual working of these two ?
    custome pipes

    viewchild vs viewchildren

    subject vs behaviouralSubject
    
    Q. component communications all scenarios?   

    custom pipe
     What is async pipe
    event emiter
    
    decorator (Angular decorators is to store metadata about a class, method, or property Class Decorators (@Component), Property Decorators (@Input()), Method Decorators (@HostListener) , Parameter Decorators (@Inject))
    
  
    what is dependency injection? (dependency consumer and dependency provider)

    What is directives :
    
   ( Directives are classes that add new behavior or modify the existing behavior to the elements in the template.
    
     to manipulate the DOM	adding/removing the element from DOM or changing the appearance of the DOM elements)
    
    
		Types of directives
		Component directive : component is also a directive with a template (template or templateUrls).
		Structural directive : adding and removing DOM elements. (ngIf, ngFor, ngSwitch)
		Attribute directive : Attribute directives are used to change the appearance or behavior of an element (ngStyle, ngClass, ngModel)
    
    
    
    
    
    
    What is the difference between the Component and a directive?
    Had you created a custom directive? had you created a directive in the project that you had done before? (on image click its size will be 		full screen)
  
  Q. lifecyclehooks used in projects


    Whole structure of angular? (https://www.c-sharpcorner.com/blogs/basic-structure-of-an-angular-application)
    How to show grid in angular? And how to show data in grid?  (AG Grid community)
    how to use validation in search bar?
    Types of event handler (ng-blur ng-change ng-click ng-copy ng-cut ng-dblclick ng-focus ng-keydown ng-keypress ng-keyup ng-mousedown 			       	ng-mouseenter ng-mouseleave ng-mousemove ng-mouseover ng-mouseup ng-paste )



    How to handle error in angular? Syntax (class ErrorHandler {  handleError(error: any): void})  (catchError, throwError in interceptor)
    
    
    How would you validate a form in angular?

    How would you display the data in the frontend in angular?
   
    create two different modules and components inside them. communicate in between with the help of subject.
    what is main.js polyfill.js vendor.js
    
    what is -o in command ng s -o?
    difference between angular 8 and 9?
     Explain latest features of the angular version you are working on ?

    **************************************************************


    Forms:
    what is form validation

    Which form you use template driven or reactive forms
    What are validators in Angular? How to implement it?
    Q. In case of multi-step forms, how will you use reactive form in it?



    **************************************************************

    Routing:

    what is Routing.. routing module configuration (switch between these views without losing the application state and properties)
    What is router-outlet  (navigation done by router-outlet)
    wild card route (to handle the invalid URLs.)
    How to protect the routes?
    routeGuard ( Angular guards: CanActivate, CanActivateChild, CanLoad, CanDeactivate and Resolve.)
    
    What is authguard ( to protect the routes from unauthorized access in angular)
    What is lazy loading, how to implement lazy loading

	(Lazy loading is a technique that allows you to load JavaScript components asynchronously when a specific route is activated.)\\\




    **************************************************************

    Module:

    what are shared modules (You can put commonly used directives, pipes, and components into one module and then import just that module 			wherever you need it in other parts of your application.)

    communication between modules?
    how to share data between two modules in angular ?

    **************************************************************

    Service:
    
    What is service file and how to use it

    how to create a service ?
    **************************************************************

    HTTP:
 
    Promise vs Observable
    which is best promise or observable ?
    callback promises observable
    what is http interceptor 
    How would you get the data from the api in angular?
 
    **************************************************************

    RxJS & NgRx:


    Q. ngrx, flow: how state, actions, selectors, etc work
    How to manage state in Angular => ngrx
    What concepts you used in rxjs
    What is rxjs, useful methods from rxjs

   

    **************************************************************

    Build:

    Explain build process of angular application    
    Difference between JIT & AOT


    **************************************************************

    Testing:



    Q. unit testing? describe different test cases for a login component with 2 input fields, submit button & cancel button


    **************************************************************

    Git and Github: 


    have you worked on Git or Git hub?
    difference between pull and push ?
    I have one lack recode in our application, how to show in web page ?
    Now am in B1 branch, I need to change B2 branch, how to change and with commit or without commit the code ?
    I did some changes in my code, so need to change another branch without commit, how will you able to do ? (edited)

    **************************************************************


    
  

    Scenario:

    **explain following code:
    import { NgModule } from '@angular/core';
    import { BrowserModule } from '@angular/platform-browser';
    @NgModule({
    imports:     [ BrowserModule ],
    providers:   [ Logger ],
    declarations: [ AppComponent ],
    exports:     [ AppComponent ],
    bootstrap:   [ AppComponent ]
    })
    export class AppModule { }


    Q. is it possible to initialize variables in a constructor

    3api call- if get response from all , then only page should be load

    Scenario 1:- You have a dropdown in that you have options of cities. If you click on the city you would get the data as name and category. So how would you display the data in of the categories and name in a card.

    Scenario 2:- In a project, If you have three modules:- AppModule,ModuleA,ModuleB. and If you run the application the AppModule would be loaded and if i go to Module A, the module A would be loaded. After that i clear the cache memory and reload the application. Then if go directly on ModuleB. It would load moduleA and ModuleB. So what would be the mistake that had might done by the developer.


    As we can also import the services in the components directly by creating the object of that services. So why we are using the dependency injection?


    How to select multiple data from drop-down
    If we want to search any data after entering 3 character How to implement that?

    If you have a huge data then how would you show in the frontend in angular?
    
    How would you implement sorting and filtering if you have got a huge amount of data in your table or grid.


   **************************************************************












