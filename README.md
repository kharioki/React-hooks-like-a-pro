## React-hooks-like-a-pro

### useMemo

*The Good*
- prevents rerendering when memoized values are not changed

*Why not memoize everything*
- performance and memory overheads
- useMemo is called every time on render, so you're calling a new function
- increases memory as we have to store cached values

*Best use cases*
- when the function you're calling in incredibly slow - making sure it doesnt recompute with every rerender
- *referential equality* - when comparing values - in my case, I use it to only call rerender when themeStyles change


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


### useCallback

*What it does*
- Just like useMemo, it's not going to rerun the code inside of it unless certain parameters change.

*The difference between **useMemo** and **useCallback**
- **useMemo** takes a function and returns the return value of the function
- **useCallback** takes a function and returns the function passed to it

*Hence*
- since useCallback returns a function, we can actually pass parameters

*When do we use useCallback*
- if you need to worry about **referential equality**
- if for any reason, creating a function is really slow


### useContext

*Reminder*
Context is for passing down props all the way down to children without having to manually pass them to every component.


### useReducer

- like useState, it allows you to manage state and rerender a component when state changes.

*Why use useReducer*
**useReducer** provides us with a better way to handle complex state.

- it has a similar pattern to redux

