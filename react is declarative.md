### React Is Declarative

We'll get to writing React code very soon, but let's take another glimpse at it to show how it's declarative.

 	<button onClick={activateTeleporter}>Activate Teleporter</button>
      
It might seem odd, but this is valid React code and should be pretty easy to understand. Notice that there's just an onClick attribute on the button... we aren't using .addEventListener() to set up event handling with all of the steps involved to set it up. Instead, we're just declaring that we want the activateTeleporter function to run when the button is clicked.
Declarative Code Recap
Imperative code instructs JavaScript on how it should perform each step. With declarative code, we tell JavaScript what we want to be done, and let JavaScript take care of performing the steps.

React is declarative because we write the code that we want, and React is in charge of taking our declared code and performing all of the JavaScript/DOM steps to get us to our desired result.

