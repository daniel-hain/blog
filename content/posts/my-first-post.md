---
title: "Embedding cool stuff"
date: 2019-11-03T12:38:23+01:00
draft: false

---

### Finally I managed to use binder with Juniper.js



<pre data-executable>
#start binder-docker

import pandas as pd

raw_data = {'first_name': ['Jason', 'Molly', 'Tina', 'Jake', 'Amy'], 
        'last_name': ['Miller', 'Jacobson', 'Ali', 'Milner', 'Cooze'], 
        'age': [42, 52, 36, 24, 73], 
        'preTestScore': [4, 24, 31, 2, 3],
        'postTestScore': [25, 94, 57, 62, 70]}
df = pd.DataFrame(raw_data, columns = ['first_name', 'last_name', 'age', 'preTestScore', 'postTestScore'])

df

</pre>

## A really cool way to embed plots with VEGA

<iframe width="800" height="450" name="us" src="/plot/us.html" frameborder="0" scrolling="no" onload="resizeIframe(this)"></iframe>

### And another one

<iframe width="800" height="600" name="pairs" src="/plot/pairplot.html" frameborder="0" scrolling="no" onload="resizeIframe(this)"></iframe>

