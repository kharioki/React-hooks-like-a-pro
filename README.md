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
