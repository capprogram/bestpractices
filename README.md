## Programming Best Practices

To complete this tutorial:

 * go to https://jupyter.org/try
 * click "Try JupyterLab"
 * close open tabs in the Lab (not necessary, just less confusing)
 * open a terminal in the Lab (File>New>Terminal)
 * paste the following into the terminal to get the jupyter notebook:<br/>
  `wget https://raw.githubusercontent.com/capprogram/bestpractices/master/bestpractices.ipynb -P /home/jovyan/demo`


* time code using the system clock, for example: 

```python
import numpy as np
import time

init_time = time.clock()  # start clock
x = np.linspace(0,100,1000000)
y = np.sqrt(x)

elap_time = time.clock() - init_time  # finds difference

print "Time elapsed is %0.3f ms" % (elap_time*1000)  # converts to ms
```

or in ipython try using the [`%time`](https://ipython.org/ipython-doc/3/interactive/magics.html#magic-time) and [`%timeit`](https://ipython.org/ipython-doc/3/interactive/magics.html#magic-timeit) magics

__Note that for complicated code, %timeit is more reliable than time.clock(). You should use a protected version of the code if you want to run %timeit on the ipython command line (for example, you can type `import templatecodeprotected` then `%timeit templatecodeprotected.main()`).__
