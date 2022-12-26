# Model - View - Controller

This pattern is used when developing software with a human computer interface.&#x20;

The user interface is of a long-lived system is a moving target.&#x20;

When developing an interactive software system, you have to consider two aspects.&#x20;

1. Changes to the user interface should be easy, and possible at run-time
2. Adapting or porting the user interface should not impact code in the functional core of the application&#x20;

To solve the problem, divide an interactive application into three areas: processing, output and input:

* The **Model** component encapsulates core data and functionality. The model is independent of specific output representations or input behavior.&#x20;
* **View** components display information to the user. A view obtains the data it displays from the model. There can be multiple views of the model.&#x20;
* Each view has an associated **Controller** component. Controllers receive input, usually as events that denote user input from keyboard, mouse etc. Events are translated to service requests, which are sent either to the model or to the view. The user interacts with the system solely via controllers.&#x20;

Here the problem is supporting variability in user interfaces. This problem may arise when developing software systems with human-computer interaction. You can solve this problem by a strict separation of responsibilities: the core functionality of the application is separated from its user interface.

#### External Links

* [Wikipedia](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller)
* [Uncle bob about MVC - Youtube video](https://www.youtube.com/watch?v=o\_TH-Y78tt4\&t=1667s)
* Davis, Ian. ["What Are The Benefits of MVC?"](http://blog.iandavis.com/2008/12/what-are-the-benefits-of-mvc/). Internet Alchemy.&#x20;
* [The evolution of MVC and other UI architectures](http://martinfowler.com/eaaDev/uiArchs.html) from Martin Fowler.
