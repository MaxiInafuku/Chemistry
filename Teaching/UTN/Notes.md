
```python
import micropip 
await micropip.install('numpy') 
import numpy as np 
await micropip.install('matplotlib')
import matplotlib.pyplot as plt

a = np.random.rand(3,2) 
b = np.random.rand(2,5) 
print(a@b)
```

```python
fig, ax = plt.subplots()
ax.plot(a)
plt.show()
print(a)
```
