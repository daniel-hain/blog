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

[//]:  # (!!!!! FROM HERE PLOT !!!!!)

{{< rawhtml >}}

<html>
<head>
  <style>
    .vega-actions a {
        margin-right: 12px;
        color: #757575;
        font-weight: normal;
        font-size: 13px;
    }
    .error {
        color: red;
    }
  </style>
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega@5"></script>
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega-lite@3.4.0"></script>
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega-embed@4"></script>
</head>
<body>
  <div id="vis"></div>
  <script>
    (function(vegaEmbed) {
      var spec = {"config": {"view": {"width": 400, "height": 300}, "mark": {"tooltip": null}}, "data": {"url": "https://vega.github.io/vega-datasets/data/zipcodes.csv"}, "mark": {"type": "circle", "size": 3}, "encoding": {"color": {"type": "nominal", "field": "leading digit"}, "latitude": {"field": "latitude", "type": "quantitative"}, "longitude": {"field": "longitude", "type": "quantitative"}, "tooltip": {"type": "nominal", "field": "zip_code"}}, "height": 400, "projection": {"type": "albersUsa"}, "transform": [{"calculate": "substring(datum.zip_code,0,1)", "as": "leading digit"}], "width": 650, "$schema": "https://vega.github.io/schema/vega-lite/v3.4.0.json"};
      var embedOpt = {"mode": "vega-lite"};

      function showError(el, error){
          el.innerHTML = ('<div class="error" style="color:red;">'
                          + '<p>JavaScript Error: ' + error.message + '</p>'
                          + "<p>This usually means there's a typo in your chart specification. "
                          + "See the javascript console for the full traceback.</p>"
                          + '</div>');
          throw error;
      }
      const el = document.getElementById('vis');
      vegaEmbed("#vis", spec, embedOpt)
        .catch(error => showError(el, error));
    })(vegaEmbed);

  </script>
</body>
</html>
{{< /rawhtml >}}


