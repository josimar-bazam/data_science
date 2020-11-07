[![author](https://www.linkedin.com/in/josimar-bazam-146577b3/) [![](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/release/python-365/) [![GPLv3 license](https://img.shields.io/badge/License-GPLv3-blue.svg)](http://perso.crans.org/besson/LICENSE.html) [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/josimar-bazam)

<p align="center">
  <img src="https://github.com/josimar-bazam/data_science/blob/main/Screen%20Shot%202020-11-06%20at%203.43.33%20PM.png" >
</p>

# Josimar Bazam

Create Colab Data Science Testing Environment

If you like to work with data analysis or "Data Science", I will show you a very tool to do tests, create your environment without installing anything on the machine.

Colab you can create several "notebooks" and do the tests without installing anything on your machine, then access the address  [Colab](https://colab.research.google.com).


Install pandas library, run the command:

``import pandas as pd``

example time series with custom date-time format:

```import plotly.graph_objects as go

  import pandas as pd

  df = pd.read_csv('https://raw.githubusercontent.com/plotly/datasets/master/finance-charts-apple.csv')

  fig = go.Figure(go.Scatter(
     x = df['Date'],
     y = df['AAPL.High'],
))

  fig.update_layout(
      title = 'Time Series with Custom Date-Time Format',
     xaxis_tickformat = '%d %B (%a)<br>%Y'
)

  fig.show()
```


<p align="center">

 <img src="https://github.com/josimar-bazam/data_science/blob/main/Screen%20Shot%202020-11-07%20at%2012.59.14%20AM.png" >

</p>


Tickformatstops to customize for different zoom levels

```import plotly.graph_objects as go

import pandas as pd

df = pd.read_csv('https://raw.githubusercontent.com/plotly/datasets/master/finance-charts-apple.csv')

fig = go.Figure(go.Scatter(
    x = df['Date'],
    y = df['mavg']
))

fig.update_layout(
    xaxis_tickformatstops = [
        dict(dtickrange=[None, 1000], value="%H:%M:%S.%L ms"),
        dict(dtickrange=[1000, 60000], value="%H:%M:%S s"),
        dict(dtickrange=[60000, 3600000], value="%H:%M m"),
        dict(dtickrange=[3600000, 86400000], value="%H:%M h"),
        dict(dtickrange=[86400000, 604800000], value="%e. %b d"),
        dict(dtickrange=[604800000, "M1"], value="%e. %b w"),
        dict(dtickrange=["M1", "M12"], value="%b '%y M"),
        dict(dtickrange=["M12", None], value="%Y Y")
    ]
)

fig.show()

```
<p align="center">

 <img src="https://github.com/josimar-bazam/data_science/blob/main/Screen%20Shot%202020-11-07%20at%201.09.48%20AM.png" >

</p>
