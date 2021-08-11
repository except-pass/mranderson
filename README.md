# Mr. Anderson



## Quick Start

```
from mranderson import Query

q = Query()
q.add("MATCH (n)")
q.add("RETURN n LIMIT 2")
```

Under the hood, this generate the cypher query

```
' '.join(q.lines)
```




    'MATCH (n) RETURN n LIMIT 2'



Which you can run with any of the built-in convenience methods
```python
q.data() #returns result as a dictionaryu
q.create() #returns a summary of what was created
q.single() #returns the first result
q.only() #returns the only result, but throws an exception if there is not 1 and only 1 result
```
