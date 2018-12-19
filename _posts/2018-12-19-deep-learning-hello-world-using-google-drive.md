---
title: "2002: Hello Deep Leaning World! Using Google Drive"
---
### 1. Login to [Google Drive](https://drive.google.com).

Create a directory structure like below or of your preference.

<img src="./../../../../assets/images/gd-directory.png"/>

Copy Data File (.csv in this case) to the above Google Drive directory.

### 2. Open Google Colaboratory.
> Colaboratory is Jupyter notebook in the form of Software As A Service provided by Google.

You can select it from the options or click on "Connect more apps" if you don't already have it as an option.

<p align="center">
  <img src="./../../../../assets/images/gd-colab.png"/>
</p>

<p align="center">
  <img src="./../../../../assets/images/gd-add-colab.png"/>
</p>

### 3. Mount Google Drive to Colab Notebook.

**Mount the Google Drive**
{% highlight python %}

from google.colab import drive
drive.mount('/content/gdrive')

{% endhighlight %}

> You can run linux commands by prefixing the commands with an '!' exclamation.

```
# List the contents of the directory.
!ls -la /content/gdrive/My\ Drive/Deep\ Learning/Supervised\ Deep\ Learning/ANN/
```

### 4. Data Preprocessing.

{% highlight python %}

# Importing the libraries
import numpy as np
import matplotlib.pyplot as plt
import pandas as pd

# Importing the dataset
dataset = pd.read_csv('/content/gdrive/My Drive/Deep Learning/Supervised Deep Learning/ANN/Churn_Modelling.csv')
X = dataset.iloc[:, 3:13].values
y = dataset.iloc[:, 13].values

{% endhighlight %}
