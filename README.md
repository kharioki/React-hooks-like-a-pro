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
