# Titanic
Decision Tree 

# Issue - GraphViz's executables not found

```
---------------------------------------------------------------------------
InvocationException                       Traceback (most recent call last)
<ipython-input-164-fd9b55de30b1> in <module>()
----> 1 Image(graph.create_png())

e:\Program Files\Anaconda3\lib\site-packages\pydotplus\graphviz.py in <lambda>(f, prog)
   1795             self.__setattr__(
   1796                 'create_' + frmt,
-> 1797                 lambda f=frmt, prog=self.prog: self.create(format=f, prog=prog)
   1798             )
   1799             f = self.__dict__['create_' + frmt]

e:\Program Files\Anaconda3\lib\site-packages\pydotplus\graphviz.py in create(self, prog, format)
   1958             if self.progs is None:
   1959                 raise InvocationException(
-> 1960                     'GraphViz\'s executables not found')
   1961 
   1962         if prog not in self.progs:

InvocationException: GraphViz's executables not found
```

**Solution:**
[reference: stackoverflow](https://stackoverflow.com/questions/45729624/graphvizs-executables-not-found-anaconda-3)

1. Download and Install https://graphviz.gitlab.io/_pages/Download/Download_windows.html
2. conda install graphviz
3. Add graphviz installed path (C:...\graphviz\bin) to Control Panel > System and Security > System > Advanced System Settings > Environment Variables > Path > Edit > New
4. **Very Important:** Restart your Jupyter notebook/**machine(MUST)**. I tried restarting machine and it worked.
This question is answered for different OS here: Graphviz's executables are not found (Python 3.4)
