### useRef

A ref is very similar to state, in that it persists in between the renders of your component.

*Good to know*
- A ref doest not cause your component to rerender when it gets changed.

*Uses cases*
* persisting values across renders without actually rerendering
* to reference elements in your html
* to store the previous value of your state

*Tip*
- avoid using *useRef* where you can use *useState*. 