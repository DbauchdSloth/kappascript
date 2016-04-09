# kappascript

A JavaScript compiler that combines the best parts of _Babel_, _CoffeeScript_, _TypeScript_ and _PureScript_ in to one glorious, if ill advised, programming language.

---

    [#bdauchdsloth] <DbauchdSloth> kappascript is bestscript
           .-oo/+o+/:-.        
       ./+o/ossysoyhsooo-     
     .//++++sshdNmddhhmNm+    
    .//+shhddmdhdysshdmNMh    
    ssydmNNmhhyo:-:::/omMN`   
    hmNNNmdy+:/-.-:::/+odN    
    oNMNms/-....-::-://+sN    
    -hNms-.-:+shyo/+hddhy+    
    -/oh:..-/ooo+:.:yyys+-    
     .:.-...`...-...////+.    
      .....--:::://:oo+os.    
      ``-----::::/+sys++o     
        `//::::::+sssooo.     
          -+++::://++o+`      
            .:/+++oo+.        

---

# FAQ

## Just what the hell do you think you are doing?

> Yet another JavaScript compiler that combines the best parts of [Babel](https://babeljs.io/), [CoffeeScript](http://coffeescript.org/), [TypeScript](http://www.typescriptlang.org/) and [PureScript]() in to one glorious, if ill advised, programming language.

## Are you serious?

> Surprisingly, I believe I am.  Let's take a step back for a moment to see why.

#### Background

There are any number of ways to approach programming, but most paradigms or perspectives can be grouped in to one or more of the following categories:

##### _Imperative_  
An approach where the implementation is defined, and the end result is implied.  This assumes an iterative processing model and is usually executed synchronously.  In this model functions about programmer abstraction and organization, and are rarely first-class objects themselves or technically required for execution.  This approach shines for low-level system programming where efficiency and optimization are important.

##### _Declarative_  
An approach where one defines the desired results, and the implementation is implied.  This also includes the category of schema, class and type definition. This makes no assumption about how the definitions are processed, though they make many constraints on how they are interpreted.  This approach implies loose coupling between semantics and syntax.

##### _Functional_  
An approach where all expressions are considered function call.  This is a recursive approach, rather than an iterative approach and execution is typically synchronous by default.  This approach assumes very tight coupling between semantics and syntax.

##### _Eventual_  
A functional approach with an event-based model where functions are executed in response to signals, rather than called recursively.  Event-based programming is an asynchronous model of execution.

##### _Algebraic_  
A functional approach where types, associates and equality are entirely free form.  This is ultimately the most abstract and is closest to the mathematical ideal of using _first order logic_ and _lambda calculus_.

#### Motivation

I really like elements from all the more popular V8-based languages, and find each has it's sweet spot for various solutions in a typical enterprise-scale project.  They all compile (or more pedantically: _trans_-pile) to the same bytecode.  We can can be run in a standard node instance, and use _sourcemaps_ to debug.  We can pick which language we want depending on our use case and context:

__JavaScript__ is the imperative perspective. is the default assumption and common compilation output for all the other languages. It is widely supported, flexible, and efficient. It makes very little assumptions regarding programming paradigm, which allows us to readily define implementations compatible with other more rigid approaches.  It is the _metamodel_ we use implement our domain-specific models. In the typical stack, [V8]() is the common runtime, [Node]() is application container, and [Express]() is the server framework. The `npm` tool provides our package and dependency management system, and is used to install and manage all the other programming languages.

__TypeScript__ is most appropriate for _declarative_ perspectives. is terrific for defining _domain models_ and _service interfaces_.  It is the universal _schema_ in which everything else is defined and normalized.  The TypeScript definitions are in effect, our application domain's _ontology_. It's advanced compile-time type inference and features like _interfaces_ and _generic types_ promote simple and reusable code.  It is great for large projects where type safety and error checking are critical concerns. It also has comprehensive tools support for build systems like [grunt]() and [gulp]() and editors such as [SublimeText](), [Atom]() and [Visual Studio]().

__CoffeeScript__ is most appropriate for _functional_ paradigms. It great for all the glue that holds together the various more complex subsystems such as _build tasks_, _plugins_ and various isolated _function implementations_ like lambdas and callbacks.  This promotes _loose coupling_ and _programmer efficiency_. It has a simpler type system than TypeScript, but the class and inheritance semantics of CoffeeScript are a proper _subset_ of TypeScript's. This means as long as we are organized about things we can consider them compatible, as far as it goes.  While TypeScript defines the exported interfaces, CoffeeScript is more at home for internal _implementation_ code.  

 **Babel** has all the latest hotness like _generators_, _proxies_ and better introspective capabilities helpful when implementing metaprogramming techniques.  

**Babel** has all the latest hotness like _proxies_ and ? which are particularly useful for metaprogramming purposes.  This is critical to

> You can see an _effective example\*_ of a coordinated orchestration of all four languages together in the [dbasr](https://github.io/DbauchdSloth/dbasr/) project.  
_* disclaimer: I am the author_

but the overhead of getting it to all work together smoothly, while enforcing the conventions that makes this possible can be onerous.  In an effort to consolidate this logic that is currently managed by a midden heap of overly clever build tasks, build-time metaprogramming and programmer-enforced project layout and configuration conventions in to a single parser component.  Once you have done that you might as well just define and EBNF file and start compiling.  Once you are compiling, you might as well

---

# Quickstart
