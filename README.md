### bqplot
---
https://github.com/bloomberg/bqplot

```py
import bqplot

import numpy as np
from bqplot import pyplot as plt
plt.figure(1, title='Line Chart')
np.random.seed(0)
n = 200
x = np.linspace(0.0, 10.0, n)
y = np.cumsum(np.random.randn(n))
plt.plot(x, y)
plt.show()

import numpy as np
from IPython.display import display
from bqplot import (
  OrdinalScale, LinearScale, Bars, Lines, Axis, Figure
)

size = 20
np.random.seed(0)

x_data = np.arange(size)

x_ord = OrdinalScale()
y_sc = LinearScale()

bar = Bars(x=x_data, y=np.random.randn(2, size), scale={'x': x_ord, 'y': y_sc}, type='stacked')
line = Lines(x=x_data, y=np.random.randn(size), scales={'x': x_ord, 'y': y_sc},
  stroke_width=3, colors=['red'], display_legend=True, labels=['Line chart'])

ax_x = Axis(scale=x_ord, grid_lines='solid', label='X')
ax_y = Axis(scale=y_sc, orientation='vertical', tick_format='0.2f',
  grid_lines='solid', label='Y')
  
Figure(marks=[bar, line], axes=[ax_x, ax_y], title='API Example', legend_location='bottom-right')


from bqplot import *
from IPython.display import display

x_data = range(10)
y_data = [i ** 2 for i in x_data]

x_sc = LinearScale()
y_sc = LinearScale()

ax_x = Axis(label='Test X', scale=x_sc, tick_format='0.0f')
ax_y = Axis(label='Test Y', scale=y_sc,
  orientation='vertical', tick_format='0.2f')

line = Lines(x=x_data,
  y=y_data,
  scales={'x': x_sc, 'y': y_sc},
  colors=['red', 'yellow'])

fig = Figure(axes=[ax_x, ax_y], marks=[line])
display(fig)
```

```sh
pip install bqplot
conda install -c conda-forge bqplot
jupyter labextension install bqplot
git clone https://github.com/bloomberg/bqplot.git
cd bqplot
pip install -e .
jupyter nbextension install --py --symlink --sys-prefix bqplot
jupyter nbextension enbale --py --sys-prefix bqplot
pip install bqplot
jupyter labextension install @jupyter-widgets/jupyterlab-manager
jupyter labextension install bqplot
```

```
```


