# views
Experiments in describing the behavior of views.

When working with clients, it's imperative that you have good mechanisms for capturing and validating requirements. The sooner you discover a discrepancy between what the client thinks they asked for and your understanding of what you think they asked for, the less code you'll have to throw away.

I've worked for many years in the Business Process Management space, where you can use the [BPMN](http://www.bpmn.org/ "BPMN") modeling language to capture and validate requirements. Tools are available for simply "drawing" BPMN diagrams, but much more useful are tools that allow the client to actually [execute the BPMN](https://www.blueworkslive.com/home/ "Blueworks Live") and "step through" their business process definitions and insure that all of the business logic is correct. "Stepping through the process" is extremely effective in uncovering mistakes and misunderstandings.

Inspired by the usefulness of executable BPMN tools, I am longing for something similar that can be used to describe what the user experience should be for a particular "view" that is used to interact with an underlying application.

Clients often want a view to behave in a very specific way - but I have not yet found a tool that is really suited for their use. Many tools let business people design what a screen should look like, and many tools let programmers quickly prototype user interfaces, but there's a gap in the middle. Beyond what the screens should look like, the business people should be able to describe the behavior of the screens in a manner that can be validated and tested against. This project holds my effort to create such a tool.

Clients often specify views that will show additional information as their customers input information. For example, once a plan is selected, the options that are available for that plan, and for which the customer is eligible, should be displayed.

Your client's detailed description for such a view might be something like the following:
  
The initial view will allow a customer to select from plan "A", "B", or "C".
If plan "A" is selected, a view will become visible to allow the customer to select from the "A" options for which they are qualified.
The customer is eligible for "A" option "1" if the customer already has an account with us.
The customer is eligible for "A" option "2" if the customer's balance due is under $1000.
The customer cannot select both option "1" and "2" unless they live in New Mexico.

Definitions such as these are fine for simple views, but you can imagine how quickly they can become unmaintainable messes.
What I'm attempting to create are tools that will help capture and organize these descriptions in a way that will both support their validation by our clients, and in a manner that will allow us to validate that the code we produce matches these descriptions.



