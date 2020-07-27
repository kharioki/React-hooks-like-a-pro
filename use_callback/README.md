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
