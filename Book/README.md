# Setting Up Code Space


```python
!pip install surprise

```

    Collecting surprise
      Downloading surprise-0.1-py2.py3-none-any.whl.metadata (327 bytes)
    Collecting scikit-surprise (from surprise)
      Downloading scikit_surprise-1.1.4.tar.gz (154 kB)
    [2K     [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m154.4/154.4 kB[0m [31m5.2 MB/s[0m eta [36m0:00:00[0m
    [?25h  Installing build dependencies ... [?25l[?25hdone
      Getting requirements to build wheel ... [?25l[?25hdone
      Preparing metadata (pyproject.toml) ... [?25l[?25hdone
    Requirement already satisfied: joblib>=1.2.0 in /usr/local/lib/python3.12/dist-packages (from scikit-surprise->surprise) (1.5.2)
    Requirement already satisfied: numpy>=1.19.5 in /usr/local/lib/python3.12/dist-packages (from scikit-surprise->surprise) (2.0.2)
    Requirement already satisfied: scipy>=1.6.0 in /usr/local/lib/python3.12/dist-packages (from scikit-surprise->surprise) (1.16.2)
    Downloading surprise-0.1-py2.py3-none-any.whl (1.8 kB)
    Building wheels for collected packages: scikit-surprise
      Building wheel for scikit-surprise (pyproject.toml) ... [?25l[?25hdone
      Created wheel for scikit-surprise: filename=scikit_surprise-1.1.4-cp312-cp312-linux_x86_64.whl size=2611304 sha256=8af3f27e3bdb62bfdc720172a0016b35915d3e59b61a8177e6253c7d579b3569
      Stored in directory: /root/.cache/pip/wheels/75/fa/bc/739bc2cb1fbaab6061854e6cfbb81a0ae52c92a502a7fa454b
    Successfully built scikit-surprise
    Installing collected packages: scikit-surprise, surprise
    Successfully installed scikit-surprise-1.1.4 surprise-0.1





```python
# Install correct version to match libraries
!pip install numpy==1.26.4 scikit-surprise --force-reinstall
```

    Collecting numpy==1.26.4
      Downloading numpy-1.26.4-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (61 kB)
    [?25l     [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m0.0/61.0 kB[0m [31m?[0m eta [36m-:--:--[0m[2K     [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m61.0/61.0 kB[0m [31m1.7 MB/s[0m eta [36m0:00:00[0m
    [?25hCollecting scikit-surprise
      Using cached scikit_surprise-1.1.4-cp312-cp312-linux_x86_64.whl
    Collecting joblib>=1.2.0 (from scikit-surprise)
      Downloading joblib-1.5.2-py3-none-any.whl.metadata (5.6 kB)
    Collecting scipy>=1.6.0 (from scikit-surprise)
      Downloading scipy-1.16.2-cp312-cp312-manylinux2014_x86_64.manylinux_2_17_x86_64.whl.metadata (62 kB)
    [2K     [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m62.0/62.0 kB[0m [31m2.4 MB/s[0m eta [36m0:00:00[0m
    [?25hDownloading numpy-1.26.4-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (18.0 MB)
    [2K   [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m18.0/18.0 MB[0m [31m46.3 MB/s[0m eta [36m0:00:00[0m
    [?25hDownloading joblib-1.5.2-py3-none-any.whl (308 kB)
    [2K   [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m308.4/308.4 kB[0m [31m12.9 MB/s[0m eta [36m0:00:00[0m
    [?25hDownloading scipy-1.16.2-cp312-cp312-manylinux2014_x86_64.manylinux_2_17_x86_64.whl (35.7 MB)
    [2K   [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m35.7/35.7 MB[0m [31m21.8 MB/s[0m eta [36m0:00:00[0m
    [?25hInstalling collected packages: numpy, joblib, scipy, scikit-surprise
      Attempting uninstall: numpy
        Found existing installation: numpy 2.0.2
        Uninstalling numpy-2.0.2:
          Successfully uninstalled numpy-2.0.2
      Attempting uninstall: joblib
        Found existing installation: joblib 1.5.2
        Uninstalling joblib-1.5.2:
          Successfully uninstalled joblib-1.5.2
      Attempting uninstall: scipy
        Found existing installation: scipy 1.16.2
        Uninstalling scipy-1.16.2:
          Successfully uninstalled scipy-1.16.2
      Attempting uninstall: scikit-surprise
        Found existing installation: scikit-surprise 1.1.4
        Uninstalling scikit-surprise-1.1.4:
          Successfully uninstalled scikit-surprise-1.1.4
    [31mERROR: pip's dependency resolver does not currently take into account all the packages that are installed. This behaviour is the source of the following dependency conflicts.
    thinc 8.3.6 requires numpy<3.0.0,>=2.0.0, but you have numpy 1.26.4 which is incompatible.
    opencv-python-headless 4.12.0.88 requires numpy<2.3.0,>=2; python_version >= "3.9", but you have numpy 1.26.4 which is incompatible.
    opencv-contrib-python 4.12.0.88 requires numpy<2.3.0,>=2; python_version >= "3.9", but you have numpy 1.26.4 which is incompatible.
    opencv-python 4.12.0.88 requires numpy<2.3.0,>=2; python_version >= "3.9", but you have numpy 1.26.4 which is incompatible.[0m[31m
    [0mSuccessfully installed joblib-1.5.2 numpy-1.26.4 scikit-surprise-1.1.4 scipy-1.16.2





```python
# Mount Drive
from google.colab import drive
drive.mount('/content/drive')
```

    Drive already mounted at /content/drive; to attempt to forcibly remount, call drive.mount("/content/drive", force_remount=True).



```python
# Unzip docs
!unzip '/content/drive/MyDrive/CS/book_rec/Book_Rec.zip'
```

    Archive:  /content/drive/MyDrive/CS/book_rec/Book_Rec.zip
      inflating: Book Recommendation/Users.csv  
      inflating: Book Recommendation/Books.csv  
      inflating: Book Recommendation/Ratings.csv  



```python
# Import necesary libraries
import numpy as np
import pandas as pd

import matplotlib.pyplot as plt
import seaborn as sns

from surprise.model_selection import train_test_split, KFold
from surprise.prediction_algorithms.matrix_factorization import SVD

from collections import defaultdict

import warnings
warnings.filterwarnings('ignore')
```

# Create, clean and prepare Data


```python
# Define variables and read CSV
book = pd.read_csv('/content/Book Recommendation/Books.csv')
rating = pd.read_csv('/content/Book Recommendation/Ratings.csv')
user = pd.read_csv('/content/Book Recommendation/Users.csv')
```


```python
rating
```





  <div id="df-9b6b8e98-800c-45c0-bff2-560ced4d963a" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>User-ID</th>
      <th>ISBN</th>
      <th>Book-Rating</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>276725</td>
      <td>034545104X</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>276726</td>
      <td>0155061224</td>
      <td>5</td>
    </tr>
    <tr>
      <th>2</th>
      <td>276727</td>
      <td>0446520802</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>276729</td>
      <td>052165615X</td>
      <td>3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>276729</td>
      <td>0521795028</td>
      <td>6</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1149775</th>
      <td>276704</td>
      <td>1563526298</td>
      <td>9</td>
    </tr>
    <tr>
      <th>1149776</th>
      <td>276706</td>
      <td>0679447156</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1149777</th>
      <td>276709</td>
      <td>0515107662</td>
      <td>10</td>
    </tr>
    <tr>
      <th>1149778</th>
      <td>276721</td>
      <td>0590442449</td>
      <td>10</td>
    </tr>
    <tr>
      <th>1149779</th>
      <td>276723</td>
      <td>05162443314</td>
      <td>8</td>
    </tr>
  </tbody>
</table>
<p>1149780 rows × 3 columns</p>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-9b6b8e98-800c-45c0-bff2-560ced4d963a')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-9b6b8e98-800c-45c0-bff2-560ced4d963a button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-9b6b8e98-800c-45c0-bff2-560ced4d963a');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-3ba7c00e-8250-44c8-a468-47be4bae2d66">
      <button class="colab-df-quickchart" onclick="quickchart('df-3ba7c00e-8250-44c8-a468-47be4bae2d66')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-3ba7c00e-8250-44c8-a468-47be4bae2d66 button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

  <div id="id_9513d301-7694-48d3-a9b9-a4cbd56afb9c">
    <style>
      .colab-df-generate {
        background-color: #E8F0FE;
        border: none;
        border-radius: 50%;
        cursor: pointer;
        display: none;
        fill: #1967D2;
        height: 32px;
        padding: 0 0 0 0;
        width: 32px;
      }

      .colab-df-generate:hover {
        background-color: #E2EBFA;
        box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
        fill: #174EA6;
      }

      [theme=dark] .colab-df-generate {
        background-color: #3B4455;
        fill: #D2E3FC;
      }

      [theme=dark] .colab-df-generate:hover {
        background-color: #434B5C;
        box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
        filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
        fill: #FFFFFF;
      }
    </style>
    <button class="colab-df-generate" onclick="generateWithVariable('rating')"
            title="Generate code using this dataframe."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M7,19H8.4L18.45,9,17,7.55,7,17.6ZM5,21V16.75L18.45,3.32a2,2,0,0,1,2.83,0l1.4,1.43a1.91,1.91,0,0,1,.58,1.4,1.91,1.91,0,0,1-.58,1.4L9.25,21ZM18.45,9,17,7.55Zm-12,3A5.31,5.31,0,0,0,4.9,8.1,5.31,5.31,0,0,0,1,6.5,5.31,5.31,0,0,0,4.9,4.9,5.31,5.31,0,0,0,6.5,1,5.31,5.31,0,0,0,8.1,4.9,5.31,5.31,0,0,0,12,6.5,5.46,5.46,0,0,0,6.5,12Z"/>
  </svg>
    </button>
    <script>
      (() => {
      const buttonEl =
        document.querySelector('#id_9513d301-7694-48d3-a9b9-a4cbd56afb9c button.colab-df-generate');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      buttonEl.onclick = () => {
        google.colab.notebook.generateWithVariable('rating');
      }
      })();
    </script>
  </div>

    </div>
  </div>





```python
# Check value count for each rating
rating['Book-Rating'].value_counts()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>count</th>
    </tr>
    <tr>
      <th>Book-Rating</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>716109</td>
    </tr>
    <tr>
      <th>8</th>
      <td>103736</td>
    </tr>
    <tr>
      <th>10</th>
      <td>78610</td>
    </tr>
    <tr>
      <th>7</th>
      <td>76457</td>
    </tr>
    <tr>
      <th>9</th>
      <td>67541</td>
    </tr>
    <tr>
      <th>5</th>
      <td>50974</td>
    </tr>
    <tr>
      <th>6</th>
      <td>36924</td>
    </tr>
    <tr>
      <th>4</th>
      <td>8904</td>
    </tr>
    <tr>
      <th>3</th>
      <td>5996</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2759</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1770</td>
    </tr>
  </tbody>
</table>
</div><br><label><b>dtype:</b> int64</label>




```python
# Check how many books each user has rated
rating['User-ID'].value_counts()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>count</th>
    </tr>
    <tr>
      <th>User-ID</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>11676</th>
      <td>13602</td>
    </tr>
    <tr>
      <th>198711</th>
      <td>7550</td>
    </tr>
    <tr>
      <th>153662</th>
      <td>6109</td>
    </tr>
    <tr>
      <th>98391</th>
      <td>5891</td>
    </tr>
    <tr>
      <th>35859</th>
      <td>5850</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th>116180</th>
      <td>1</td>
    </tr>
    <tr>
      <th>116166</th>
      <td>1</td>
    </tr>
    <tr>
      <th>116154</th>
      <td>1</td>
    </tr>
    <tr>
      <th>116137</th>
      <td>1</td>
    </tr>
    <tr>
      <th>276723</th>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>105283 rows × 1 columns</p>
</div><br><label><b>dtype:</b> int64</label>




```python
# Check data frame
book
```





  <div id="df-a6d3cfe7-ad80-46b7-873b-e826f15360a4" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ISBN</th>
      <th>Book-Title</th>
      <th>Book-Author</th>
      <th>Year-Of-Publication</th>
      <th>Publisher</th>
      <th>Image-URL-S</th>
      <th>Image-URL-M</th>
      <th>Image-URL-L</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0195153448</td>
      <td>Classical Mythology</td>
      <td>Mark P. O. Morford</td>
      <td>2002</td>
      <td>Oxford University Press</td>
      <td>http://images.amazon.com/images/P/0195153448.0...</td>
      <td>http://images.amazon.com/images/P/0195153448.0...</td>
      <td>http://images.amazon.com/images/P/0195153448.0...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0002005018</td>
      <td>Clara Callan</td>
      <td>Richard Bruce Wright</td>
      <td>2001</td>
      <td>HarperFlamingo Canada</td>
      <td>http://images.amazon.com/images/P/0002005018.0...</td>
      <td>http://images.amazon.com/images/P/0002005018.0...</td>
      <td>http://images.amazon.com/images/P/0002005018.0...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0060973129</td>
      <td>Decision in Normandy</td>
      <td>Carlo D'Este</td>
      <td>1991</td>
      <td>HarperPerennial</td>
      <td>http://images.amazon.com/images/P/0060973129.0...</td>
      <td>http://images.amazon.com/images/P/0060973129.0...</td>
      <td>http://images.amazon.com/images/P/0060973129.0...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0374157065</td>
      <td>Flu: The Story of the Great Influenza Pandemic...</td>
      <td>Gina Bari Kolata</td>
      <td>1999</td>
      <td>Farrar Straus Giroux</td>
      <td>http://images.amazon.com/images/P/0374157065.0...</td>
      <td>http://images.amazon.com/images/P/0374157065.0...</td>
      <td>http://images.amazon.com/images/P/0374157065.0...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0393045218</td>
      <td>The Mummies of Urumchi</td>
      <td>E. J. W. Barber</td>
      <td>1999</td>
      <td>W. W. Norton &amp;amp; Company</td>
      <td>http://images.amazon.com/images/P/0393045218.0...</td>
      <td>http://images.amazon.com/images/P/0393045218.0...</td>
      <td>http://images.amazon.com/images/P/0393045218.0...</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>271355</th>
      <td>0440400988</td>
      <td>There's a Bat in Bunk Five</td>
      <td>Paula Danziger</td>
      <td>1988</td>
      <td>Random House Childrens Pub (Mm)</td>
      <td>http://images.amazon.com/images/P/0440400988.0...</td>
      <td>http://images.amazon.com/images/P/0440400988.0...</td>
      <td>http://images.amazon.com/images/P/0440400988.0...</td>
    </tr>
    <tr>
      <th>271356</th>
      <td>0525447644</td>
      <td>From One to One Hundred</td>
      <td>Teri Sloat</td>
      <td>1991</td>
      <td>Dutton Books</td>
      <td>http://images.amazon.com/images/P/0525447644.0...</td>
      <td>http://images.amazon.com/images/P/0525447644.0...</td>
      <td>http://images.amazon.com/images/P/0525447644.0...</td>
    </tr>
    <tr>
      <th>271357</th>
      <td>006008667X</td>
      <td>Lily Dale : The True Story of the Town that Ta...</td>
      <td>Christine Wicker</td>
      <td>2004</td>
      <td>HarperSanFrancisco</td>
      <td>http://images.amazon.com/images/P/006008667X.0...</td>
      <td>http://images.amazon.com/images/P/006008667X.0...</td>
      <td>http://images.amazon.com/images/P/006008667X.0...</td>
    </tr>
    <tr>
      <th>271358</th>
      <td>0192126040</td>
      <td>Republic (World's Classics)</td>
      <td>Plato</td>
      <td>1996</td>
      <td>Oxford University Press</td>
      <td>http://images.amazon.com/images/P/0192126040.0...</td>
      <td>http://images.amazon.com/images/P/0192126040.0...</td>
      <td>http://images.amazon.com/images/P/0192126040.0...</td>
    </tr>
    <tr>
      <th>271359</th>
      <td>0767409752</td>
      <td>A Guided Tour of Rene Descartes' Meditations o...</td>
      <td>Christopher  Biffle</td>
      <td>2000</td>
      <td>McGraw-Hill Humanities/Social Sciences/Languages</td>
      <td>http://images.amazon.com/images/P/0767409752.0...</td>
      <td>http://images.amazon.com/images/P/0767409752.0...</td>
      <td>http://images.amazon.com/images/P/0767409752.0...</td>
    </tr>
  </tbody>
</table>
<p>271360 rows × 8 columns</p>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-a6d3cfe7-ad80-46b7-873b-e826f15360a4')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-a6d3cfe7-ad80-46b7-873b-e826f15360a4 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-a6d3cfe7-ad80-46b7-873b-e826f15360a4');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-aecf778a-61ed-4256-b135-cde1048b9c5c">
      <button class="colab-df-quickchart" onclick="quickchart('df-aecf778a-61ed-4256-b135-cde1048b9c5c')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-aecf778a-61ed-4256-b135-cde1048b9c5c button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

  <div id="id_f319b1f8-8195-4bfe-963d-92d991b0caaf">
    <style>
      .colab-df-generate {
        background-color: #E8F0FE;
        border: none;
        border-radius: 50%;
        cursor: pointer;
        display: none;
        fill: #1967D2;
        height: 32px;
        padding: 0 0 0 0;
        width: 32px;
      }

      .colab-df-generate:hover {
        background-color: #E2EBFA;
        box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
        fill: #174EA6;
      }

      [theme=dark] .colab-df-generate {
        background-color: #3B4455;
        fill: #D2E3FC;
      }

      [theme=dark] .colab-df-generate:hover {
        background-color: #434B5C;
        box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
        filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
        fill: #FFFFFF;
      }
    </style>
    <button class="colab-df-generate" onclick="generateWithVariable('book')"
            title="Generate code using this dataframe."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M7,19H8.4L18.45,9,17,7.55,7,17.6ZM5,21V16.75L18.45,3.32a2,2,0,0,1,2.83,0l1.4,1.43a1.91,1.91,0,0,1,.58,1.4,1.91,1.91,0,0,1-.58,1.4L9.25,21ZM18.45,9,17,7.55Zm-12,3A5.31,5.31,0,0,0,4.9,8.1,5.31,5.31,0,0,0,1,6.5,5.31,5.31,0,0,0,4.9,4.9,5.31,5.31,0,0,0,6.5,1,5.31,5.31,0,0,0,8.1,4.9,5.31,5.31,0,0,0,12,6.5,5.46,5.46,0,0,0,6.5,12Z"/>
  </svg>
    </button>
    <script>
      (() => {
      const buttonEl =
        document.querySelector('#id_f319b1f8-8195-4bfe-963d-92d991b0caaf button.colab-df-generate');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      buttonEl.onclick = () => {
        google.colab.notebook.generateWithVariable('book');
      }
      })();
    </script>
  </div>

    </div>
  </div>





```python
# Merge and create DF, drop duplicates and only keep the ones with ratings on the left (rating)
df = pd.merge(rating, book.drop_duplicates(['ISBN']), on='ISBN', how='left')
```


```python
# Drop unecessary columns
df.drop(['Image-URL-S', 'Image-URL-M', 'Image-URL-L'], axis=1, inplace=True)
```


```python
# Check new DF
df
```





  <div id="df-852d46cc-2a8f-4000-8dfc-da08007a2e1c" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>User-ID</th>
      <th>ISBN</th>
      <th>Book-Rating</th>
      <th>Book-Title</th>
      <th>Book-Author</th>
      <th>Year-Of-Publication</th>
      <th>Publisher</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>276725</td>
      <td>034545104X</td>
      <td>0</td>
      <td>Flesh Tones: A Novel</td>
      <td>M. J. Rose</td>
      <td>2002</td>
      <td>Ballantine Books</td>
    </tr>
    <tr>
      <th>1</th>
      <td>276726</td>
      <td>0155061224</td>
      <td>5</td>
      <td>Rites of Passage</td>
      <td>Judith Rae</td>
      <td>2001</td>
      <td>Heinle</td>
    </tr>
    <tr>
      <th>2</th>
      <td>276727</td>
      <td>0446520802</td>
      <td>0</td>
      <td>The Notebook</td>
      <td>Nicholas Sparks</td>
      <td>1996</td>
      <td>Warner Books</td>
    </tr>
    <tr>
      <th>3</th>
      <td>276729</td>
      <td>052165615X</td>
      <td>3</td>
      <td>Help!: Level 1</td>
      <td>Philip Prowse</td>
      <td>1999</td>
      <td>Cambridge University Press</td>
    </tr>
    <tr>
      <th>4</th>
      <td>276729</td>
      <td>0521795028</td>
      <td>6</td>
      <td>The Amsterdam Connection : Level 4 (Cambridge ...</td>
      <td>Sue Leather</td>
      <td>2001</td>
      <td>Cambridge University Press</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1149775</th>
      <td>276704</td>
      <td>1563526298</td>
      <td>9</td>
      <td>Get Clark Smart : The Ultimate Guide for the S...</td>
      <td>Clark Howard</td>
      <td>2000</td>
      <td>Longstreet Press</td>
    </tr>
    <tr>
      <th>1149776</th>
      <td>276706</td>
      <td>0679447156</td>
      <td>0</td>
      <td>Eight Weeks to Optimum Health: A Proven Progra...</td>
      <td>Andrew Weil</td>
      <td>1997</td>
      <td>Alfred A. Knopf</td>
    </tr>
    <tr>
      <th>1149777</th>
      <td>276709</td>
      <td>0515107662</td>
      <td>10</td>
      <td>The Sherbrooke Bride (Bride Trilogy (Paperback))</td>
      <td>Catherine Coulter</td>
      <td>1996</td>
      <td>Jove Books</td>
    </tr>
    <tr>
      <th>1149778</th>
      <td>276721</td>
      <td>0590442449</td>
      <td>10</td>
      <td>Fourth Grade Rats</td>
      <td>Jerry Spinelli</td>
      <td>1996</td>
      <td>Scholastic</td>
    </tr>
    <tr>
      <th>1149779</th>
      <td>276723</td>
      <td>05162443314</td>
      <td>8</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>1149780 rows × 7 columns</p>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-852d46cc-2a8f-4000-8dfc-da08007a2e1c')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-852d46cc-2a8f-4000-8dfc-da08007a2e1c button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-852d46cc-2a8f-4000-8dfc-da08007a2e1c');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-1723c4b8-c419-41c5-a3c0-3f74f06baa2b">
      <button class="colab-df-quickchart" onclick="quickchart('df-1723c4b8-c419-41c5-a3c0-3f74f06baa2b')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-1723c4b8-c419-41c5-a3c0-3f74f06baa2b button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

  <div id="id_7d4790bb-6761-4a84-aee0-fab35bcacc6a">
    <style>
      .colab-df-generate {
        background-color: #E8F0FE;
        border: none;
        border-radius: 50%;
        cursor: pointer;
        display: none;
        fill: #1967D2;
        height: 32px;
        padding: 0 0 0 0;
        width: 32px;
      }

      .colab-df-generate:hover {
        background-color: #E2EBFA;
        box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
        fill: #174EA6;
      }

      [theme=dark] .colab-df-generate {
        background-color: #3B4455;
        fill: #D2E3FC;
      }

      [theme=dark] .colab-df-generate:hover {
        background-color: #434B5C;
        box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
        filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
        fill: #FFFFFF;
      }
    </style>
    <button class="colab-df-generate" onclick="generateWithVariable('df')"
            title="Generate code using this dataframe."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M7,19H8.4L18.45,9,17,7.55,7,17.6ZM5,21V16.75L18.45,3.32a2,2,0,0,1,2.83,0l1.4,1.43a1.91,1.91,0,0,1,.58,1.4,1.91,1.91,0,0,1-.58,1.4L9.25,21ZM18.45,9,17,7.55Zm-12,3A5.31,5.31,0,0,0,4.9,8.1,5.31,5.31,0,0,0,1,6.5,5.31,5.31,0,0,0,4.9,4.9,5.31,5.31,0,0,0,6.5,1,5.31,5.31,0,0,0,8.1,4.9,5.31,5.31,0,0,0,12,6.5,5.46,5.46,0,0,0,6.5,12Z"/>
  </svg>
    </button>
    <script>
      (() => {
      const buttonEl =
        document.querySelector('#id_7d4790bb-6761-4a84-aee0-fab35bcacc6a button.colab-df-generate');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      buttonEl.onclick = () => {
        google.colab.notebook.generateWithVariable('df');
      }
      })();
    </script>
  </div>

    </div>
  </div>





```python
# Rename columns for better handling
df.rename(columns={'Book-Rating': 'rating', 'ISBN': 'book_id','User-ID': 'user_id' }, inplace=True)
```


```python
# Check data integrity
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 1149780 entries, 0 to 1149779
    Data columns (total 7 columns):
     #   Column               Non-Null Count    Dtype 
    ---  ------               --------------    ----- 
     0   user_id              1149780 non-null  int64 
     1   book_id              1149780 non-null  object
     2   rating               1149780 non-null  int64 
     3   Book-Title           1031136 non-null  object
     4   Book-Author          1031134 non-null  object
     5   Year-Of-Publication  1031136 non-null  object
     6   Publisher            1031134 non-null  object
    dtypes: int64(2), object(5)
    memory usage: 61.4+ MB


**Observations**:

- The rating data contains 11,49,780 observations and 7 columns.
- The 'user id' and 'rating' columns are both of numeric data type.
- The book id column has the data type object. We'll convert it to string format. As we will be using this column in subsequent steps
- We have some ISBN that do not exist in our book DF

**Distribution of ratings**


```python
# Change book id object to string
df['book_id'] = df['book_id'].astype(str)
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 1149780 entries, 0 to 1149779
    Data columns (total 7 columns):
     #   Column               Non-Null Count    Dtype 
    ---  ------               --------------    ----- 
     0   user_id              1149780 non-null  int64 
     1   book_id              1149780 non-null  object
     2   rating               1149780 non-null  int64 
     3   Book-Title           1031136 non-null  object
     4   Book-Author          1031134 non-null  object
     5   Year-Of-Publication  1031136 non-null  object
     6   Publisher            1031134 non-null  object
    dtypes: int64(2), object(5)
    memory usage: 61.4+ MB



```python
# Visualize our ratings
plt.figure(figsize=(12,4))
sns.countplot(data = df, x= 'rating')
```




    <Axes: xlabel='rating', ylabel='count'>




    
![png](output_21_1.png)
    


**Observations:**

- We mostly have books with 0 ratings, aproximately 700000.
- It is best for us to remove all 0 ratings, to eliminate the bias.


```python
# As 0s are missing ratings, we drop them to avoid issues
df.drop(df.index[df['rating'] == 0], inplace = True)
```


```python
# Now we plot again
# Visualize our ratings
plt.figure(figsize=(12,4))
sns.countplot(data = df, x= 'rating')
```




    <Axes: xlabel='rating', ylabel='count'>




    
![png](output_24_1.png)
    


**Obbservations:**
- Our most common rating is 8.
- We have few negative reviews.


```python
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Index: 433671 entries, 1 to 1149779
    Data columns (total 7 columns):
     #   Column               Non-Null Count   Dtype 
    ---  ------               --------------   ----- 
     0   user_id              433671 non-null  int64 
     1   book_id              433671 non-null  object
     2   rating               433671 non-null  int64 
     3   Book-Title           383842 non-null  object
     4   Book-Author          383840 non-null  object
     5   Year-Of-Publication  383842 non-null  object
     6   Publisher            383840 non-null  object
    dtypes: int64(2), object(5)
    memory usage: 26.5+ MB



```python
df.user_id.nunique()
```




    77805




```python
df.book_id.nunique()
```




    185973




```python
# How many books have each user rated?
df.groupby(['user_id','book_id']).count()
```





  <div id="df-3f2e527e-1aba-4c8f-ac58-ccbf12a5a88c" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th></th>
      <th>rating</th>
      <th>Book-Title</th>
      <th>Book-Author</th>
      <th>Year-Of-Publication</th>
      <th>Publisher</th>
    </tr>
    <tr>
      <th>user_id</th>
      <th>book_id</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="5" valign="top">8</th>
      <th>0002005018</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>074322678X</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>0887841740</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1552041778</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1567407781</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th rowspan="5" valign="top">278854</th>
      <th>0375703063</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>042516098X</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>0425163393</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>0553275739</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>0553579606</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>433671 rows × 5 columns</p>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-3f2e527e-1aba-4c8f-ac58-ccbf12a5a88c')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-3f2e527e-1aba-4c8f-ac58-ccbf12a5a88c button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-3f2e527e-1aba-4c8f-ac58-ccbf12a5a88c');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-cfac262a-23ac-4135-a6f3-372ed186039f">
      <button class="colab-df-quickchart" onclick="quickchart('df-cfac262a-23ac-4135-a6f3-372ed186039f')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-cfac262a-23ac-4135-a6f3-372ed186039f button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

    </div>
  </div>





```python
# Lets count ratings for the same book
df.book_id.value_counts()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>count</th>
    </tr>
    <tr>
      <th>book_id</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0316666343</th>
      <td>707</td>
    </tr>
    <tr>
      <th>0971880107</th>
      <td>581</td>
    </tr>
    <tr>
      <th>0385504209</th>
      <td>487</td>
    </tr>
    <tr>
      <th>0312195516</th>
      <td>383</td>
    </tr>
    <tr>
      <th>0679781587</th>
      <td>333</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th>0140441905</th>
      <td>1</td>
    </tr>
    <tr>
      <th>0886777267</th>
      <td>1</td>
    </tr>
    <tr>
      <th>0671697951</th>
      <td>1</td>
    </tr>
    <tr>
      <th>0553560956</th>
      <td>1</td>
    </tr>
    <tr>
      <th>05162443314</th>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>185973 rows × 1 columns</p>
</div><br><label><b>dtype:</b> int64</label>




```python
# Check and plot the ratings of the most popular book
df[df['book_id'] == '0316666343']['rating'].value_counts().plot(kind='bar')
```




    <Axes: xlabel='rating'>




    
![png](output_31_1.png)
    


**Observations:**

- We can see that the majority of the ratings for this book are 8, followed by 9, 10, and then 7.
- Because the count of ratings 1, 2, 3, and 4 is much lower than ratings 8, 9, and 10, this implies that the book is liked by the majority of users.


```python
df.user_id.value_counts()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>count</th>
    </tr>
    <tr>
      <th>user_id</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>11676</th>
      <td>8524</td>
    </tr>
    <tr>
      <th>98391</th>
      <td>5802</td>
    </tr>
    <tr>
      <th>153662</th>
      <td>1969</td>
    </tr>
    <tr>
      <th>189835</th>
      <td>1906</td>
    </tr>
    <tr>
      <th>23902</th>
      <td>1395</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th>114079</th>
      <td>1</td>
    </tr>
    <tr>
      <th>114081</th>
      <td>1</td>
    </tr>
    <tr>
      <th>114096</th>
      <td>1</td>
    </tr>
    <tr>
      <th>114115</th>
      <td>1</td>
    </tr>
    <tr>
      <th>276723</th>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>77805 rows × 1 columns</p>
</div><br><label><b>dtype:</b> int64</label>



**Observations:**

The user with user_id: 11676 has interacted with the most number of books, i.e., 8524 times.
But still, there is a possibility of 185973-8524 = 177449 more interactions as we have 185973 unique books in the dataset.

# Data Preparation

As we have noted, the dataset is quite large, computational efficiency is crucial for the development of the model. There are many users who have only rated a few books and also books which are rated by very few users. Hence, as many books have few ratings, we can drop them to make a better model.

We'll be taking books that have at least 50 ratings.


```python
# Create column of users as a panda series
users = df.user_id
users
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>user_id</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>276726</td>
    </tr>
    <tr>
      <th>3</th>
      <td>276729</td>
    </tr>
    <tr>
      <th>4</th>
      <td>276729</td>
    </tr>
    <tr>
      <th>6</th>
      <td>276736</td>
    </tr>
    <tr>
      <th>7</th>
      <td>276737</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th>1149773</th>
      <td>276704</td>
    </tr>
    <tr>
      <th>1149775</th>
      <td>276704</td>
    </tr>
    <tr>
      <th>1149777</th>
      <td>276709</td>
    </tr>
    <tr>
      <th>1149778</th>
      <td>276721</td>
    </tr>
    <tr>
      <th>1149779</th>
      <td>276723</td>
    </tr>
  </tbody>
</table>
<p>433671 rows × 1 columns</p>
</div><br><label><b>dtype:</b> int64</label>




```python
# Create dictionary for users, add tthem iif they are not there
ratings_count = dict()
for user in users:
  if user in ratings_count:
    ratings_count[user] += 1
  else:
    ratings_count[user] = 1
```


```python
from os import remove
# Cut users that have less than 50 reviews
RATINGS_CUTOFF = 50
remove_users = []
for user, ratings in ratings_count.items():
  if ratings < RATINGS_CUTOFF:
    remove_users.append(user)
```


```python
# Remove them
df = df.loc[-df.user_id.isin(remove_users)]
```


```python
# Check new shape
df.shape
```




    (175023, 7)




```python
# Repeat process for books
books = df.book_id
ratings_count = dict()

for book in books:
  if book in ratings_count:
    ratings_count[book] += 1
  else:
    ratings_count[book] = 1
```


```python
ratings_count
```




    {'030700645X': 4,
     '0307127923': 5,
     '0307302016': 3,
     '0307302636': 6,
     '0307987655': 3,
     '0316563242': 1,
     '039480001X': 16,
     '0394800028': 9,
     '0394800184': 10,
     '039480029X': 12,
     '039480967X': 7,
     '0394925696': 2,
     '0439083702': 1,
     '0439213592': 1,
     '0439242363': 1,
     '0439449316': 1,
     '0590386522': 1,
     '0590402218': 2,
     '0590404342': 1,
     '0590442619': 1,
     '0590442791': 3,
     '0590442805': 3,
     '0590442899': 1,
     '059044297X': 4,
     '059046602X': 2,
     '0590466577': 1,
     '0590629719': 3,
     '0590921622': 1,
     '0590965492': 1,
     '0689845405': 1,
     '0689847564': 1,
     '0717283194': 5,
     '0717283208': 6,
     '0717283275': 2,
     '0717283364': 4,
     '0717283372': 3,
     '0717284832': 4,
     '0717284972': 3,
     '0717287017': 2,
     '0717287106': 2,
     '0721452728': 1,
     '0736401113': 1,
     '0761406158': 1,
     '0769600239': 1,
     '0785316477': 1,
     '0785316493': 1,
     '0785316531': 1,
     '087701759X': 3,
     '0895777010': 1,
     '1561452718': 1,
     '1562826468': 4,
     '2764104936': 1,
     '002542730X': 28,
     '003008685X': 1,
     '0060006641': 3,
     '0060542128': 9,
     '0061009059': 45,
     '0062507109': 1,
     '0132220598': 1,
     '0140283374': 2,
     '014039026X': 1,
     '0140390715': 1,
     '0141439742': 2,
     '0152050167': 7,
     '0201000822': 1,
     '0310435706': 1,
     '0312944691': 2,
     '0316776963': 41,
     '033031582': 4,
     '0345413903': 20,
     '0375408886': 1,
     '0375751513': 8,
     '0380702843': 15,
     '0380791978': 12,
     '038081904X': 3,
     '0385424736': 21,
     '0385486804': 18,
     '0385503857': 11,
     '0385504209': 106,
     '039304016X': 1,
     '0394738136': 1,
     '0394862147': 1,
     '0399149562': 6,
     '0399225064': 1,
     '0399501487': 49,
     '0425047962': 2,
     '0425104338': 11,
     '0425116840': 11,
     '0425133516': 12,
     '0425190749': 4,
     '0440185327': 10,
     '0440224764': 37,
     '0440236061': 7,
     '0440236738': 10,
     '0440428130': 7,
     '0441627404': 11,
     '0446311677': 1,
     '0446325503': 2,
     '0446350982': 11,
     '0446522384': 3,
     '0446600415': 4,
     '0446608890': 13,
     '0446676640': 2,
     '0451180739': 4,
     '0451191153': 7,
     '0451203593': 7,
     '0452284449': 20,
     '0471018732': 1,
     '0517573636': 2,
     '0523485964': 1,
     '0552137030': 15,
     '0553078925': 2,
     '0553280368': 37,
     '0553351672': 2,
     '0553571656': 13,
     '0553573926': 10,
     '0553574566': 11,
     '0553581929': 7,
     '0670307254': 1,
     '0671014420': 4,
     '0671037692': 1,
     '0671528904': 9,
     '067172021X': 2,
     '0671727079': 2,
     '0671740504': 5,
     '0671749897': 2,
     '0671876821': 7,
     '0679417648': 5,
     '0679419853': 2,
     '0679731148': 17,
     '0679736042': 12,
     '0684869098': 1,
     '0715388185': 2,
     '0718002067': 1,
     '0736903054': 5,
     '0740723367': 11,
     '0743406176': 5,
     '0743412028': 17,
     '0743422082': 6,
     '0743444477': 8,
     '0743457943': 9,
     '0767903382': 6,
     '0785243038': 2,
     '0786866845': 9,
     '0800757483': 1,
     '0802425488': 2,
     '0803653719': 1,
     '0805018956': 1,
     '0810909650': 5,
     '0811802981': 17,
     '0811811409': 10,
     '0812504798': 4,
     '0812531353': 5,
     '0836210263': 10,
     '0836213076': 2,
     '0836217691': 16,
     '0836218515': 12,
     '0836218817': 13,
     '0836221192': 7,
     '0836221311': 8,
     '0836236688': 7,
     '084233338X': 1,
     '0842370668': 1,
     '0843947888': 3,
     '0849995892': 1,
     '0871890917': 1,
     '087605534X': 2,
     '0877790426': 1,
     '087784870X': 1,
     '0887621112': 2,
     '0890814082': 1,
     '0890876517': 9,
     '0890876967': 2,
     '0897330536': 2,
     '0898155843': 2,
     '0898157803': 8,
     '0898793912': 3,
     '0898794080': 1,
     '0898794544': 1,
     '0898796601': 1,
     '089879661X': 1,
     '0898797055': 1,
     '0912452161': 1,
     '0932592007': 3,
     '0964420805': 1,
     '0965035214': 2,
     '0967201519': 1,
     '1400060265': 5,
     '1559586893': 4,
     '1562923668': 2,
     '1564403963': 1,
     '1565075722': 2,
     '1568380593': 1,
     '156865037X': 3,
     '1572302399': 1,
     '1572304510': 3,
     '1576733343': 2,
     '1576739597': 1,
     '1581690606': 2,
     '1852303468': 1,
     '1930285000': 1,
     '8251800811': 4,
     '0060008350': 1,
     '0060572965': 4,
     '0061020028': 2,
     '0061031410': 10,
     '0061094129': 5,
     '0312983433': 3,
     '0345440064': 4,
     '0345545571': 1,
     '0380731851': 27,
     '0380820889': 9,
     '038533558X': 12,
     '0399142649': 3,
     '0440221048': 2,
     '0446527041': 8,
     '0446531588': 5,
     '0446610607': 1,
     '0446612510': 2,
     '0449006522': 13,
     '0449219364': 30,
     '0449221512': 29,
     '0449227545': 5,
     '0451179153': 3,
     '0451179897': 3,
     '0451188950': 1,
     '0451202473': 4,
     '0451204301': 5,
     '0451206525': 11,
     '0515125490': 3,
     '0515129038': 4,
     '0515130389': 21,
     '0515135968': 8,
     '0553582364': 6,
     '0671001795': 43,
     '0671658301': 1,
     '0671891537': 1,
     '0684810387': 8,
     '068815333X': 3,
     '0743206045': 16,
     '0743417836': 2,
     '0786889667': 5,
     '0805060251': 1,
     '0812528042': 2,
     '1551667517': 7,
     '1551669625': 5,
     '7099300799': 1,
     '7100100699': 1,
     '7100100750': 1,
     '7678300699': 1,
     '780446525800': 1,
     '0060002492': 4,
     '0061057894': 7,
     '0140067647': 4,
     '0140350144': 1,
     '0310239826': 1,
     '0312088027': 1,
     '0345257596': 2,
     '0345274695': 3,
     '0345331044': 1,
     '0345337662': 77,
     '0373079001': 1,
     '037308935X': 1,
     '0373089376': 1,
     '0373115377': 1,
     '0373115431': 5,
     '0374475067': 1,
     '0380429780': 2,
     '0380600129': 13,
     '0380708655': 4,
     '0425065553': 5,
     '0425189082': 2,
     '0425194876': 1,
     '0440111188': 1,
     '0440844444': 1,
     '0440940001': 18,
     '0441094880': 1,
     '0446606812': 38,
     '0449209830': 3,
     '0449702634': 1,
     '0515094978': 5,
     '055325698X': 4,
     '0553287532': 12,
     '0590434160': 1,
     '0670894508': 8,
     '0671434225': 4,
     '0671525808': 9,
     '0671745093': 2,
     '0684846675': 1,
     '0802400086': 2,
     '0804106304': 51,
     '0812533518': 2,
     '0825428688': 2,
     '0842339337': 1,
     '0842354220': 1,
     '0879050470': 1,
     '088419597X': 3,
     '0895774011': 1,
     '0899669492': 1,
     '1556611536': 3,
     '1558744150': 28,
     '1558745017': 10,
     '1576739562': 1,
     '1582293031': 1,
     '373219350': 1,
     '373219377': 1,
     '373219407': 1,
     '373219415': 1,
     '37321944X': 1,
     '373219458': 1,
     '0156005891': 13,
     '0316171565': 2,
     '0373218192': 12,
     '0373223218': 1,
     '0373244487': 11,
     '0373272898': 4,
     '037327291X': 2,
     '0373290861': 2,
     '0373441762': 4,
     '0373441851': 4,
     '0373484003': 13,
     '0373762380': 1,
     '0440122090': 14,
     '044022103X': 17,
     '0440223571': 7,
     '0440225701': 34,
     '0446603589': 13,
     '0451180348': 2,
     '0515124621': 10,
     '0553574477': 1,
     '0590424939': 1,
     '0590424971': 2,
     '0590433474': 1,
     '0590433865': 2,
     '0590436414': 1,
     '0590436597': 1,
     '0590437216': 1,
     '0590439006': 1,
     '0590448331': 1,
     '0590456490': 1,
     '0590523562': 1,
     '0670877514': 1,
     '0671644459': 5,
     '0671644475': 8,
     '0689800975': 2,
     '0743410181': 5,
     '0778320022': 2,
     '0778320065': 4,
     '0778320286': 1,
     '080410946X': 6,
     '0821714600': 1,
     '0821715402': 1,
     '0821774638': 2,
     '082177574X': 1,
     '1551660679': 1,
     '1551661586': 5,
     '1551664992': 2,
     '1551665220': 2,
     '1551665344': 6,
     '1551666960': 3,
     '1551667487': 2,
     '1557485534': 1,
     '0006542808': 1,
     '0060392185': 1,
     '0140367209': 1,
     '0140546499': 2,
     '0146000579': 4,
     '0146000706': 1,
     '0146000994': 1,
     '0146001109': 1,
     '0192816071': 1,
     '0307022196': 1,
     '0310912520': 1,
     '0312850131': 1,
     '0312860862': 1,
     '0312923651': 1,
     '0312970234': 3,
     '0321096983': 1,
     '0345300742': 3,
     '0345318617': 1,
     '0345334590': 1,
     '0345352459': 8,
     '0345369335': 10,
     '0345431464': 1,
     '037302973X': 1,
     '0373071388': 1,
     '0373074646': 1,
     '0373106939': 1,
     '0373110138': 2,
     '0373112572': 1,
     '0373117868': 1,
     '0373122772': 3,
     '0373167318': 1,
     '0373708335': 1,
     '037383375X': 1,
     '0375756817': 1,
     '0380710870': 4,
     '038097391X': 2,
     '0385320329': 1,
     '0394800168': 13,
     '0394820371': 24,
     '0395681863': 1,
     '0399122400': 1,
     '0399134883': 2,
     '0425048543': 3,
     '042513525X': 20,
     '0425140032': 11,
     '0425178102': 9,
     '042518630X': 17,
     '0439040825': 1,
     '0440139791': 2,
     '0440184622': 7,
     '0440206561': 2,
     '0440207622': 13,
     '0440479002': 6,
     '044056753X': 2,
     '0440800129': 2,
     '0440920833': 1,
     '0441116183': 1,
     '0441470734': 1,
     '0445205636': 1,
     '0446520608': 1,
     '0446603368': 1,
     '0449210324': 1,
     '0451136683': 2,
     '0451173392': 2,
     '0515131229': 33,
     '051788710X': 2,
     '0553131834': 3,
     '0553201344': 1,
     '0553202790': 1,
     '0553271571': 1,
     '0553282700': 2,
     '0553297988': 5,
     '0553299352': 2,
     '0553565605': 1,
     '0590117653': 1,
     '0590413848': 2,
     '059046244X': 1,
     '0590466178': 1,
     '059088008X': 3,
     '0671017128': 6,
     '0671019961': 2,
     '0671502522': 4,
     '0671556843': 4,
     '067160550X': 1,
     '0671655450': 2,
     '0671663755': 2,
     '0671721623': 2,
     '0671775715': 3,
     '0684174707': 1,
     '0684832860': 2,
     '0684835614': 2,
     '0689828896': 1,
     '0786862572': 8,
     '0800786092': 1,
     '0812055721': 1,
     '0812502076': 1,
     '0812504321': 2,
     '0812508084': 3,
     '0812511840': 1,
     '0812523466': 2,
     '0812531558': 1,
     '0812533232': 1,
     '0812543181': 1,
     '0821713655': 1,
     '0821726595': 1,
     '0848706978': 1,
     '0865926433': 1,
     '0871318156': 3,
     '0880380845': 3,
     '088184781X': 2,
     '0886775981': 6,
     '0890817596': 1,
     '0898151899': 3,
     '155882068X': 1,
     '1569751544': 1,
     '1570423008': 1,
     '100940/86': 1,
     '127420/98': 1,
     '13440/86': 1,
     '1351394403': 1,
     '140274871': 1,
     '15019/87': 1,
     '16560/87': 1,
     '16785/87': 1,
     '18128/87': 1,
     '18678/87': 1,
     '19973/88': 1,
     '203671/03': 1,
     '2070567842': 2,
     '23950/88': 1,
     '30623/89': 1,
     '36388/90': 1,
     '40052/90': 1,
     '40614/2098': 1,
     '71837/93': 1,
     '75666/95': 1,
     '77556/94': 1,
     '80651/94': 1,
     '8401422825': 1,
     '8440630794': 2,
     '847223973X': 1,
     '8476409419': 1,
     '8497890663': 1,
     '8585362693': 1,
     '8585443464': 1,
     '9714511081': 1,
     '9721028800': 1,
     '9721033561': 1,
     '9721035130': 1,
     '9722013831': 1,
     '9722020242': 1,
     '9722105507': 1,
     '9722113747': 1,
     '9722319914': 2,
     '9722330950': 1,
     '9722902628': 1,
     '972370403X': 1,
     '9723706504': 1,
     '9724114384': 1,
     '9724128725': 1,
     '9724129411': 1,
     '9724131009': 1,
     '9724502023': 1,
     '9724508552': 1,
     '9724509524': 1,
     '97245146089': 1,
     '9726080630': 1,
     '9726081327': 1,
     '9726081378': 2,
     '9726081424': 1,
     '9726101034': 1,
     '9726593855': 1,
     '9726653525': 1,
     '9726991366': 1,
     '9726993474': 1,
     '9727100112': 1,
     '9727110541': 1,
     '9728305729': 2,
     '9728313039': 1,
     '9728440006': 1,
     '9728440030': 1,
     '9728440057': 1,
     '9728440138': 1,
     '9728440170': 1,
     '9728440200': 1,
     '9728440324': 1,
     '9728440383': 1,
     '9728440405': 1,
     '9728440456': 1,
     '9728440642': 1,
     '9728440693': 1,
     '9728440804': 1,
     '9728487002': 1,
     '9728487142': 1,
     '9728487150': 1,
     '9728487266': 1,
     '9728487304': 1,
     '9728487355': 1,
     '9728487576': 1,
     '9728487606': 1,
     '9728487614': 1,
     '9728515227': 1,
     '9729720495': 1,
     '972975831X': 1,
     '9729817715': 1,
     '9729852405': 1,
     '9748440537': 1,
     '0060502320': 2,
     '0060934700': 9,
     '0060976977': 5,
     '0064471047': 24,
     '0066238501': 8,
     '0142001740': 72,
     '0312863934': 2,
     '0373033605': 1,
     '0373162669': 1,
     '0373226063': 5,
     '0373226144': 7,
     '0373243944': 2,
     '0373243979': 1,
     '0373709889': 1,
     '0373810431': 1,
     '0373810601': 1,
     '0373834446': 5,
     '0373834489': 4,
     '0373836023': 2,
     '0375756469': 1,
     '037582345X': 5,
     '0375823468': 2,
     '0380730448': 2,
     '0380789035': 36,
     '0380810492': 2,
     '0380817845': 4,
     '0380973634': 3,
     '0380973650': 11,
     '0380973839': 1,
     '0380977281': 4,
     '038097827X': 3,
     '0399146431': 19,
     '0439064864': 63,
     '0439064872': 54,
     '0439136350': 64,
     '0439136369': 43,
     '0439139597': 64,
     '0446341932': 3,
     '0451167317': 37,
     '0451406176': 2,
     '0451409256': 5,
     '0451524934': 34,
     '0451526341': 28,
     '0553263633': 3,
     '0553280325': 5,
     '0590353403': 57,
     '0618002219': 17,
     '0618002227': 25,
     '0671021001': 48,
     '0679781587': 85,
     '0679879242': 7,
     '0681415207': 1,
     '1556520743': 1,
     '156389226X': 1,
     '1563895730': 4,
     '1567310877': 2,
     '156971620X': 4,
     '1931081727': 4,
     '0060164662': 2,
     '0060191929': 4,
     '0140107649': 3,
     '0140128107': 1,
     '0151000719': 3,
     '0151001006': 3,
     '0316603287': 20,
     '0316666343': 145,
     '0316693006': 15,
     '0316693200': 28,
     '0316769487': 58,
     '0316779423': 12,
     '0316779490': 7,
     '0316789089': 17,
     '0316969443': 19,
     '0345339711': 25,
     '0345428900': 1,
     '0375400699': 1,
     '0380978539': 1,
     '0385420161': 13,
     '0385470819': 5,
     '0385500769': 1,
     '0385505833': 37,
     '0394574745': 3,
     '0399148582': 3,
     '0425184129': 3,
     '0446523569': 11,
     '0446525502': 8,
     '0446525537': 12,
     '0446527793': 10,
     '0446531332': 19,
     '0525943862': 2,
     '052594463X': 1,
     '0609605925': 6,
     '0609606727': 4,
     '0670892963': 24,
     '0671042556': 7,
     '0679410430': 3,
     '0679419624': 2,
     '0679442790': 10,
     '0679603352': 3,
     '067972768X': 4,
     '0679732241': 5,
     '0679746048': 32,
     '0684874318': 1,
     '0688180639': 4,
     '0743230051': 5,
     '0842336214': 1,
     '1558747028': 5,
     '1558747346': 4,
     '1570717257': 2,
     '0006510345': 3,
     '0007100221': 1,
     '0061092606': 11,
     '0099449943': 1,
     '0140292918': 1,
     '0140366660': 2,
     '0140366857': 2,
     '0140482202': 1,
     '0140622063': 5,
     '0198604025': 1,
     '0261102214': 4,
     '0349102155': 2,
     '0416196772': 1,
     '0552546933': 6,
     '0552771090': 3,
     '057120354X': 1,
     '0571209521': 1,
     '0671894455': 14,
     '0743222229': 9,
     '0743462335': 1,
     '0747538069': 1,
     '0749391308': 5,
     '0749396067': 5,
     '0752804510': 2,
     '0753507579': 1,
     '0753807327': 1,
     '0890877564': 2,
     '0947782230': 1,
     '1405200677': 1,
     '1405401184': 1,
     '1841150355': 1,
     '1841950521': 1,
     '1841952931': 1,
     '1842040405': 1,
     '1853260002': 7,
     '185479549X': 1,
     '1854795554': 1,
     '1858813093': 1,
     '190178424X': 1,
     '2020315491': 1,
     '2070322068': 1,
     '2070375617': 1,
     '2070393577': 1,
     '2229137939': 1,
     '2253000868': 1,
     '2253001457': 2,
     '2253002895': 2,
     '2253006866': 1,
     '2253037796': 1,
     '2253043974': 3,
     '2253046922': 1,
     '2253049417': 5,
     '2253051381': 1,
     '2253063339': 5,
     '2253140872': 3,
     '2253148539': 1,
     '2253170127': 1,
     '2253170372': 1,
     '2253170569': 1,
     '2253171077': 2,
     '2702418112': 1,
     '2737329787': 1,
     '2742722771': 1,
     '2857043821': 1,
     '2868696945': 3,
     '2871290911': 1,
     '2876915618': 1,
     '2876916193': 1,
     '2909051196': 1,
     '000636988X': 1,
     '0006642004': 1,
     '0060562080': 4,
     '0060928336': 64,
     '0099254611': 1,
     '0099385716': 2,
     '0099427974': 3,
     '009969221X': 2,
     '0099755114': 4,
     '0140562109': 1,
     '0140563733': 2,
     '0140620915': 1,
     '0141182571': 1,
     '0142000663': 16,
     '0142300128': 1,
     '0146003241': 2,
     '0330258648': 6,
     '0330306839': 7,
     '0380012863': 22,
     '0385600526': 1,
     '0394404289': 7,
     '0434971383': 1,
     '0552106615': 2,
     '0552107735': 2,
     '0552108812': 2,
     '055211804': 2,
     '0552124753': 20,
     '0552996009': 9,
     '0552998001': 14,
     '0552999504': 2,
     '0552999512': 1,
     '0575073004': 3,
     '0575073314': 2,
     '058242092X': 1,
     '0586210687': 1,
     '0613117905': 1,
     '0679883878': 1,
     '068484267X': 35,
     '070121015X': 1,
     '0722159676': 2,
     '0743225082': 9,
     '0744531500': 1,
     '074603010X': 1,
     '0749397543': 15,
     '0749720182': 2,
     '0749725028': 1,
     '0752853007': 1,
     '0805067868': 1,
     '0811828379': 1,
     '0861638522': 1,
     '0006513204': 5,
     '0099771519': 24,
     '0140621725': 2,
     '014143984X': 1,
     '0330367358': 11,
     '0375726322': 2,
     '0752853694': 5,
     '0786889373': 3,
     '1857988132': 2,
     '2020291541': 2,
     '2070360024': 9,
     '2070360423': 2,
     '2070364283': 1,
     '2070375161': 3,
     '2070412571': 1,
     '2070415686': 4,
     '2070417700': 1,
     '2070426815': 1,
     '2070513726': 1,
     '2070544281': 1,
     '2207245810': 1,
     '2207250474': 1,
     '2207251756': 1,
     '2207252000': 3,
     '2253001295': 2,
     '2253004898': 2,
     '2253005274': 4,
     '2253009164': 1,
     '2253051020': 2,
     '2253152064': 1,
     '2253152277': 1,
     '2258036992': 1,
     '2264027681': 1,
     '2264028815': 1,
     '2266000489': 2,
     '2266022504': 3,
     '2266085778': 1,
     '2266120158': 1,
     '226612269X': 2,
     '2290305251': 1,
     '2290307831': 1,
     '2290314110': 1,
     '2290331406': 1,
     '2290337382': 2,
     '2707318094': 1,
     '2723407381': 1,
     '2723407403': 1,
     '2723407411': 1,
     '2723409821': 1,
     '273811167X': 1,
     '287129478X': 1,
     '2871294798': 1,
     '0060000805': 1,
     '0060512822': 7,
     '0060730552': 3,
     '0060930535': 40,
     '0061015725': 14,
     '0061030015': 2,
     '0061056871': 5,
     '0061097314': 14,
     '0140185844': 1,
     '0140255087': 4,
     '0142001430': 31,
     '0142003581': 1,
     '0151002290': 2,
     '0151004137': 1,
     '0156001314': 14,
     '0156006332': 1,
     '0224018256': 2,
     '031215125X': 4,
     '0312420366': 4,
     '0316291161': 5,
     '0316353299': 2,
     '0330291610': 1,
     '0330357808': 1,
     '033036197X': 2,
     '0330391763': 1,
     '0330483013': 1,
     '033390785X': 1,
     '0345439481': 2,
     '0345450515': 1,
     '0375725296': 1,
     '0380603764': 5,
     '0385319452': 4,
     '0385336403': 1,
     '0385720106': 34,
     '039914255X': 6,
     '044652719X': 1,
     '0451526988': 1,
     '0451527569': 1,
     '0531301427': 2,
     '0553295071': 4,
     '0590988301': 1,
     '0595157939': 1,
     '0606006133': 1,
     '0606011773': 2,
     '0618446877': 1,
     '0671646575': 5,
     '0671776134': 14,
     '0676974562': 2,
     '0702231088': 1,
     '0743228480': 1,
     '0743234413': 1,
     '0743418735': 5,
     '0743431014': 3,
     '0746020120': 1,
     '0747265097': 2,
     '075350507X': 1,
     '0767902521': 29,
     '0812541979': 1,
     '0881104086': 1,
     '1400060648': 2,
     '1585672939': 1,
     '1585673625': 1,
     '1592247865': 1,
     '1841955469': 1,
     '1860491235': 1,
     '1876825251': 1,
     '0060536705': 3,
     '0061042005': 8,
     '0061083275': 1,
     '0061095869': 3,
     '0312968256': 1,
     '0312983824': 15,
     '0316089699': 9,
     '0345447840': 12,
     '0373079621': 2,
     '0373121601': 1,
     '0373121709': 1,
     '0373121857': 1,
     '0373168438': 2,
     '0373169299': 2,
     '0373195036': 1,
     '0373196636': 3,
     '0373218400': 9,
     '0373224818': 1,
     '0373226934': 3,
     '0373226950': 1,
     '0373240228': 6,
     '0373242328': 11,
     '037325928X': 2,
     '0373259840': 3,
     '0373271867': 1,
     '0373273193': 2,
     '0373301529': 1,
     '0373301537': 1,
     '037330174X': 1,
     '0373700474': 1,
     '0373703023': 1,
     '0373706200': 1,
     '0373706545': 3,
     '0373706901': 2,
     '0373707959': 3,
     '037370822X': 1,
     '0373708300': 2,
     '0373708319': 2,
     '0373708351': 2,
     '0373764146': 1,
     '037383232X': 1,
     '0373835426': 1,
     '0373871864': 2,
     '0373871945': 1,
     '038076735X': 1,
     '0380775840': 6,
     '0380777304': 2,
     '0425181111': 3,
     '0440168724': 11,
     '0440225868': 1,
     '0446346438': 1,
     '0446357405': 7,
     '0446364762': 8,
     '0446527130': 6,
     '0446603082': 5,
     '0449210197': 1,
     '0451205189': 2,
     '0451205650': 5,
     '0451207963': 2,
     '0505522969': 1,
     '0505524333': 3,
     '050552435X': 2,
     '0515118230': 13,
     '0515130419': 1,
     '051513287X': 27,
     '0517077744': 3,
     '0553107232': 2,
     '0553267159': 2,
     '0553285947': 4,
     '055329945X': 2,
     '0553562746': 5,
     '0553574078': 7,
     '0553584898': 3,
     '059035342X': 90,
     '0671007696': 8,
     '0671521446': 3,
     '067179793X': 4,
     '0689856644': 2,
     '0743412621': 5,
     '0743431367': 2,
     '0743467191': 1,
     '0821740121': 1,
     '0821768107': 2,
     '0828003882': 1,
     '0843948078': 2,
     ...}




```python
# We have less books than users, we set up a smaller threshold
RATINGS_CUTOFF = 10
remove_books = []
for book, num_ratings in ratings_count.items():
  if num_ratings < RATINGS_CUTOFF:
    remove_books.append(book)
# We remove the books
df = df.loc[-df.book_id.isin(remove_books)]
```


```python
df.shape
```




    (26698, 7)




```python
# Check our data, to see how many books and users have been removed
df.nunique()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>user_id</th>
      <td>1257</td>
    </tr>
    <tr>
      <th>book_id</th>
      <td>1497</td>
    </tr>
    <tr>
      <th>rating</th>
      <td>10</td>
    </tr>
    <tr>
      <th>Book-Title</th>
      <td>1367</td>
    </tr>
    <tr>
      <th>Book-Author</th>
      <td>587</td>
    </tr>
    <tr>
      <th>Year-Of-Publication</th>
      <td>43</td>
    </tr>
    <tr>
      <th>Publisher</th>
      <td>204</td>
    </tr>
  </tbody>
</table>
</div><br><label><b>dtype:</b> int64</label>




```python
count_interactions = df.groupby('user_id').count()['book_id']
```


```python
sns.histplot(count_interactions)
```




    <Axes: xlabel='book_id', ylabel='Count'>




    
![png](output_47_1.png)
    


**Obbservations:**
- We can see that the distribution is skewed to the right
- We have few books wth many ratings

# Model building

# Model 1: Rank-Based Reccomendation system
- Rank-based recommendation systems provide recommendations based on the most popular items. This kind of recommendation system is useful when we have cold start problems.
- To build it, we take average of all the ratings provided to each book and then rank them based on their average rating. Allso taking in consideration, the amount of reviews.


```python
# Get the mean rating of every book
average_rating = df.groupby('book_id')['rating'].mean()
average_rating
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>rating</th>
    </tr>
    <tr>
      <th>book_id</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0020442203</th>
      <td>8.727273</td>
    </tr>
    <tr>
      <th>002542730X</th>
      <td>7.428571</td>
    </tr>
    <tr>
      <th>0028604199</th>
      <td>8.000000</td>
    </tr>
    <tr>
      <th>0060002050</th>
      <td>7.800000</td>
    </tr>
    <tr>
      <th>006000438X</th>
      <td>7.666667</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th>1573229725</th>
      <td>9.117647</td>
    </tr>
    <tr>
      <th>1576737330</th>
      <td>7.437500</td>
    </tr>
    <tr>
      <th>1592400876</th>
      <td>8.840000</td>
    </tr>
    <tr>
      <th>1878424319</th>
      <td>7.111111</td>
    </tr>
    <tr>
      <th>1931561648</th>
      <td>9.200000</td>
    </tr>
  </tbody>
</table>
<p>1497 rows × 1 columns</p>
</div><br><label><b>dtype:</b> float64</label>




```python
# As the numbber of ratings is also an important factor, we will create that variable
count_rating = df.groupby('book_id')['rating'].count()
count_rating
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>rating</th>
    </tr>
    <tr>
      <th>book_id</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0020442203</th>
      <td>11</td>
    </tr>
    <tr>
      <th>002542730X</th>
      <td>28</td>
    </tr>
    <tr>
      <th>0028604199</th>
      <td>10</td>
    </tr>
    <tr>
      <th>0060002050</th>
      <td>10</td>
    </tr>
    <tr>
      <th>006000438X</th>
      <td>15</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th>1573229725</th>
      <td>17</td>
    </tr>
    <tr>
      <th>1576737330</th>
      <td>16</td>
    </tr>
    <tr>
      <th>1592400876</th>
      <td>25</td>
    </tr>
    <tr>
      <th>1878424319</th>
      <td>18</td>
    </tr>
    <tr>
      <th>1931561648</th>
      <td>10</td>
    </tr>
  </tbody>
</table>
<p>1497 rows × 1 columns</p>
</div><br><label><b>dtype:</b> int64</label>




```python
# We merge this data Frames into a final one
final_rating = pd.DataFrame({'avg_rating': average_rating, 'rating_count': count_rating})
final_rating
```





  <div id="df-d5d40192-0ce1-49cf-9a42-e76c2db7ddd2" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>avg_rating</th>
      <th>rating_count</th>
    </tr>
    <tr>
      <th>book_id</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0020442203</th>
      <td>8.727273</td>
      <td>11</td>
    </tr>
    <tr>
      <th>002542730X</th>
      <td>7.428571</td>
      <td>28</td>
    </tr>
    <tr>
      <th>0028604199</th>
      <td>8.000000</td>
      <td>10</td>
    </tr>
    <tr>
      <th>0060002050</th>
      <td>7.800000</td>
      <td>10</td>
    </tr>
    <tr>
      <th>006000438X</th>
      <td>7.666667</td>
      <td>15</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1573229725</th>
      <td>9.117647</td>
      <td>17</td>
    </tr>
    <tr>
      <th>1576737330</th>
      <td>7.437500</td>
      <td>16</td>
    </tr>
    <tr>
      <th>1592400876</th>
      <td>8.840000</td>
      <td>25</td>
    </tr>
    <tr>
      <th>1878424319</th>
      <td>7.111111</td>
      <td>18</td>
    </tr>
    <tr>
      <th>1931561648</th>
      <td>9.200000</td>
      <td>10</td>
    </tr>
  </tbody>
</table>
<p>1497 rows × 2 columns</p>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-d5d40192-0ce1-49cf-9a42-e76c2db7ddd2')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-d5d40192-0ce1-49cf-9a42-e76c2db7ddd2 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-d5d40192-0ce1-49cf-9a42-e76c2db7ddd2');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-44edead0-eed2-4e64-9448-5d5a8ed7019e">
      <button class="colab-df-quickchart" onclick="quickchart('df-44edead0-eed2-4e64-9448-5d5a8ed7019e')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-44edead0-eed2-4e64-9448-5d5a8ed7019e button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

  <div id="id_740cf0f9-617c-487f-bc17-5e5fd54597a9">
    <style>
      .colab-df-generate {
        background-color: #E8F0FE;
        border: none;
        border-radius: 50%;
        cursor: pointer;
        display: none;
        fill: #1967D2;
        height: 32px;
        padding: 0 0 0 0;
        width: 32px;
      }

      .colab-df-generate:hover {
        background-color: #E2EBFA;
        box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
        fill: #174EA6;
      }

      [theme=dark] .colab-df-generate {
        background-color: #3B4455;
        fill: #D2E3FC;
      }

      [theme=dark] .colab-df-generate:hover {
        background-color: #434B5C;
        box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
        filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
        fill: #FFFFFF;
      }
    </style>
    <button class="colab-df-generate" onclick="generateWithVariable('final_rating')"
            title="Generate code using this dataframe."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M7,19H8.4L18.45,9,17,7.55,7,17.6ZM5,21V16.75L18.45,3.32a2,2,0,0,1,2.83,0l1.4,1.43a1.91,1.91,0,0,1,.58,1.4,1.91,1.91,0,0,1-.58,1.4L9.25,21ZM18.45,9,17,7.55Zm-12,3A5.31,5.31,0,0,0,4.9,8.1,5.31,5.31,0,0,0,1,6.5,5.31,5.31,0,0,0,4.9,4.9,5.31,5.31,0,0,0,6.5,1,5.31,5.31,0,0,0,8.1,4.9,5.31,5.31,0,0,0,12,6.5,5.46,5.46,0,0,0,6.5,12Z"/>
  </svg>
    </button>
    <script>
      (() => {
      const buttonEl =
        document.querySelector('#id_740cf0f9-617c-487f-bc17-5e5fd54597a9 button.colab-df-generate');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      buttonEl.onclick = () => {
        google.colab.notebook.generateWithVariable('final_rating');
      }
      })();
    </script>
  </div>

    </div>
  </div>





```python
# Lets look at the rating count
final_rating.rating_count.value_counts()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>count</th>
    </tr>
    <tr>
      <th>rating_count</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>10</th>
      <td>237</td>
    </tr>
    <tr>
      <th>11</th>
      <td>196</td>
    </tr>
    <tr>
      <th>12</th>
      <td>161</td>
    </tr>
    <tr>
      <th>13</th>
      <td>114</td>
    </tr>
    <tr>
      <th>14</th>
      <td>104</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th>70</th>
      <td>1</td>
    </tr>
    <tr>
      <th>47</th>
      <td>1</td>
    </tr>
    <tr>
      <th>77</th>
      <td>1</td>
    </tr>
    <tr>
      <th>145</th>
      <td>1</td>
    </tr>
    <tr>
      <th>68</th>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>65 rows × 1 columns</p>
</div><br><label><b>dtype:</b> int64</label>




```python
# For a cold start problem, we will create a funmction that recomends the best rated books
def top_n_books(data, n, min_interactions=100):
  # Books wiith minimum number of interactions
  recommendations = data[data.rating_count > min_interactions]
  # Sort values with average rating
  recommendations = recommendations.sort_values(by='avg_rating', ascending=False)
  return recommendations.index[:n]
```


```python
# Lets use the function to find the top 5 books
res = top_n_books(final_rating, 5, 10)
list_of_books = []
for i in res:
  list_of_books.append(df[df['book_id'] == str(i)]['Book-Title'].unique()[0])
list_of_books
```




    ['The Two Towers (The Lord of the Rings, Part 2)',
     'Harry Potter and the Chamber of Secrets Postcard Book',
     "My Sister's Keeper : A Novel (Picoult, Jodi)",
     'The Giving Tree',
     'A Tree Grows in Brooklyn']




```python
# Lets use the function to find the top 5 books that have at least 100 interactions
res2 = top_n_books(final_rating, 5, 100)
list_of_books = []
for i in res2:
  list_of_books.append(df[df['book_id'] == str(i)]['Book-Title'].unique()[0])
list_of_books
```




    ['The Da Vinci Code', 'The Lovely Bones: A Novel']



# Model 2: Colaborative filtering Recommendation System
In this type of recommendation system, we do not need any information about the users or items. We only need user-item interaction data to build a collaborative recommendation system, in ths case the ratings provided by the users.

We will build a similarity-based recommendation system using cosine similarity and using KNN to find similar users who are the nearest neighbor to the given user.


```python
# Import methods and functions from surprise
from surprise import accuracy
from surprise.reader import Reader
from surprise.dataset import Dataset

from surprise.model_selection import GridSearchCV
from surprise.prediction_algorithms.knns import KNNBasic
```


```python
# Function to get precision and recall from a modell provided
def precision_recall_at_k(model, k=10, threshold=0.7):
  # Map predictions to each user
  user_est_true = defaultdict(list)
  # Make predictions on test data
  predictions = model.test(testset)

  for uid, _, true_r, est, _ in predictions:
    user_est_true[uid].append((est, true_r))

  precisions = dict()
  recalls = dict()
  for uid, user_ratings in user_est_true.items():
    # Sort user ratings
    user_ratings.sort(key=lambda x: x[0], reverse=True)
    # Number of relevant items
    n_rel = sum((true_r >= threshold for (_, true_r) in user_ratings))
    # Number of recommended items in top k
    n_rec_k = sum(((est >= threshold) for (est, _) in user_ratings[:k]))
    # Number of relevant and recommended items in top K
    n_rel_and_rec_k = sum((true_r >= threshold) and (est >= threshold)
                      for (est, true_r) in user_ratings[:k])
    # Precision@K: Proportion of recommended items that are relevant
    # When n_rec_k is 0, Precision is undefined. We here set Precision to 0 when n_rec_k is 0
    precisions[uid] = n_rel_and_rec_k / n_rec_k if n_rec_k != 0 else 0
    recalls[uid] = n_rel_and_rec_k / n_rel if n_rel != 0 else 0
  # Mean of all predicted precisions
  precision = round(sum(prec for prec in precisions.values()) / len(precisions))
  # Mean of al predicted recalls
  recall = round(sum(rec for rec in recalls.values()) / len(recalls), 3)
  accuracy.rmse(predictions)
  # Print and compute F1 Score
  print(f'Precision: {precision}')
  print(f'Recall: {recall}')
  f1 = 2 * (precision * recall) / (precision + recall)
  print(f'F1 score: {round(f1, 3)}')
```


```python
# We will encode the user and bokk id, for simplicity
from sklearn.preprocessing import LabelEncoder
data = df[['user_id', 'book_id']].apply(LabelEncoder().fit_transform)
data['rating'] = df['rating']
data
```





  <div id="df-21af7d66-4f00-4661-b3e8-e097cbc7933c" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>user_id</th>
      <th>book_id</th>
      <th>rating</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1211</th>
      <td>1251</td>
      <td>521</td>
      <td>9</td>
    </tr>
    <tr>
      <th>1213</th>
      <td>1251</td>
      <td>524</td>
      <td>9</td>
    </tr>
    <tr>
      <th>1214</th>
      <td>1251</td>
      <td>525</td>
      <td>8</td>
    </tr>
    <tr>
      <th>1456</th>
      <td>1252</td>
      <td>1</td>
      <td>10</td>
    </tr>
    <tr>
      <th>1474</th>
      <td>1252</td>
      <td>52</td>
      <td>9</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1149564</th>
      <td>1250</td>
      <td>928</td>
      <td>7</td>
    </tr>
    <tr>
      <th>1149581</th>
      <td>1250</td>
      <td>1288</td>
      <td>9</td>
    </tr>
    <tr>
      <th>1149592</th>
      <td>1250</td>
      <td>1316</td>
      <td>7</td>
    </tr>
    <tr>
      <th>1149627</th>
      <td>1250</td>
      <td>1483</td>
      <td>10</td>
    </tr>
    <tr>
      <th>1149637</th>
      <td>1250</td>
      <td>1496</td>
      <td>9</td>
    </tr>
  </tbody>
</table>
<p>26698 rows × 3 columns</p>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-21af7d66-4f00-4661-b3e8-e097cbc7933c')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-21af7d66-4f00-4661-b3e8-e097cbc7933c button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-21af7d66-4f00-4661-b3e8-e097cbc7933c');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-295736b8-9628-41da-848b-4c16400b319f">
      <button class="colab-df-quickchart" onclick="quickchart('df-295736b8-9628-41da-848b-4c16400b319f')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-295736b8-9628-41da-848b-4c16400b319f button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

  <div id="id_7da45535-effb-425e-a89d-d284cbcd356f">
    <style>
      .colab-df-generate {
        background-color: #E8F0FE;
        border: none;
        border-radius: 50%;
        cursor: pointer;
        display: none;
        fill: #1967D2;
        height: 32px;
        padding: 0 0 0 0;
        width: 32px;
      }

      .colab-df-generate:hover {
        background-color: #E2EBFA;
        box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
        fill: #174EA6;
      }

      [theme=dark] .colab-df-generate {
        background-color: #3B4455;
        fill: #D2E3FC;
      }

      [theme=dark] .colab-df-generate:hover {
        background-color: #434B5C;
        box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
        filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
        fill: #FFFFFF;
      }
    </style>
    <button class="colab-df-generate" onclick="generateWithVariable('data')"
            title="Generate code using this dataframe."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M7,19H8.4L18.45,9,17,7.55,7,17.6ZM5,21V16.75L18.45,3.32a2,2,0,0,1,2.83,0l1.4,1.43a1.91,1.91,0,0,1,.58,1.4,1.91,1.91,0,0,1-.58,1.4L9.25,21ZM18.45,9,17,7.55Zm-12,3A5.31,5.31,0,0,0,4.9,8.1,5.31,5.31,0,0,0,1,6.5,5.31,5.31,0,0,0,4.9,4.9,5.31,5.31,0,0,0,6.5,1,5.31,5.31,0,0,0,8.1,4.9,5.31,5.31,0,0,0,12,6.5,5.46,5.46,0,0,0,6.5,12Z"/>
  </svg>
    </button>
    <script>
      (() => {
      const buttonEl =
        document.querySelector('#id_7da45535-effb-425e-a89d-d284cbcd356f button.colab-df-generate');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      buttonEl.onclick = () => {
        google.colab.notebook.generateWithVariable('data');
      }
      })();
    </script>
  </div>

    </div>
  </div>





```python
# Create copy for further use
df_rating = data.copy()
```


```python
# Calculate average
average_rating = data.groupby('book_id').mean()['rating']
# Calculate count of ratings
count_rating = data.groupby('book_id').count()['rating']
# Update final rating
final_rating = pd.DataFrame({'avg_rating': average_rating, 'rating_count': count_rating})
final_rating
```





  <div id="df-cbb82bc2-a18f-4c84-917d-53cabebeed6e" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>avg_rating</th>
      <th>rating_count</th>
    </tr>
    <tr>
      <th>book_id</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>8.727273</td>
      <td>11</td>
    </tr>
    <tr>
      <th>1</th>
      <td>7.428571</td>
      <td>28</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8.000000</td>
      <td>10</td>
    </tr>
    <tr>
      <th>3</th>
      <td>7.800000</td>
      <td>10</td>
    </tr>
    <tr>
      <th>4</th>
      <td>7.666667</td>
      <td>15</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1492</th>
      <td>9.117647</td>
      <td>17</td>
    </tr>
    <tr>
      <th>1493</th>
      <td>7.437500</td>
      <td>16</td>
    </tr>
    <tr>
      <th>1494</th>
      <td>8.840000</td>
      <td>25</td>
    </tr>
    <tr>
      <th>1495</th>
      <td>7.111111</td>
      <td>18</td>
    </tr>
    <tr>
      <th>1496</th>
      <td>9.200000</td>
      <td>10</td>
    </tr>
  </tbody>
</table>
<p>1497 rows × 2 columns</p>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-cbb82bc2-a18f-4c84-917d-53cabebeed6e')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-cbb82bc2-a18f-4c84-917d-53cabebeed6e button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-cbb82bc2-a18f-4c84-917d-53cabebeed6e');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-b798837c-a7d2-4e01-95de-aa5ff990ea3a">
      <button class="colab-df-quickchart" onclick="quickchart('df-b798837c-a7d2-4e01-95de-aa5ff990ea3a')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-b798837c-a7d2-4e01-95de-aa5ff990ea3a button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

  <div id="id_97d99cd3-7717-4e99-ac86-3871b64d9e84">
    <style>
      .colab-df-generate {
        background-color: #E8F0FE;
        border: none;
        border-radius: 50%;
        cursor: pointer;
        display: none;
        fill: #1967D2;
        height: 32px;
        padding: 0 0 0 0;
        width: 32px;
      }

      .colab-df-generate:hover {
        background-color: #E2EBFA;
        box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
        fill: #174EA6;
      }

      [theme=dark] .colab-df-generate {
        background-color: #3B4455;
        fill: #D2E3FC;
      }

      [theme=dark] .colab-df-generate:hover {
        background-color: #434B5C;
        box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
        filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
        fill: #FFFFFF;
      }
    </style>
    <button class="colab-df-generate" onclick="generateWithVariable('final_rating')"
            title="Generate code using this dataframe."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M7,19H8.4L18.45,9,17,7.55,7,17.6ZM5,21V16.75L18.45,3.32a2,2,0,0,1,2.83,0l1.4,1.43a1.91,1.91,0,0,1,.58,1.4,1.91,1.91,0,0,1-.58,1.4L9.25,21ZM18.45,9,17,7.55Zm-12,3A5.31,5.31,0,0,0,4.9,8.1,5.31,5.31,0,0,0,1,6.5,5.31,5.31,0,0,0,4.9,4.9,5.31,5.31,0,0,0,6.5,1,5.31,5.31,0,0,0,8.1,4.9,5.31,5.31,0,0,0,12,6.5,5.46,5.46,0,0,0,6.5,12Z"/>
  </svg>
    </button>
    <script>
      (() => {
      const buttonEl =
        document.querySelector('#id_97d99cd3-7717-4e99-ac86-3871b64d9e84 button.colab-df-generate');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      buttonEl.onclick = () => {
        google.colab.notebook.generateWithVariable('final_rating');
      }
      })();
    </script>
  </div>

    </div>
  </div>





```python
# We change the format of the dataset, to be able to use the surprise library
reader = Reader(rating_scale=(1,10))
data = Dataset.load_from_df(data[['user_id', 'book_id', 'rating']], reader)
```


```python
# We split the data
trainset, testset = train_test_split(data, test_size=0.3, random_state=42)
```

**User-Based Collaborative Filtering**


```python
# Define the algorithm used and if it is user based
sim_options = {
    'name': 'cosine',
    'user_based': True
}
# Use KNNBasic with our similarity options
algo_knn_user = KNNBasic(sim_options = sim_options, verbose = False)
# Train the algorithm and predict for testset
algo_knn_user.fit(trainset)
```




    <surprise.prediction_algorithms.knns.KNNBasic at 0x7b60476b8890>




```python
# Use previous function to obtain precision, recall and f1 score
precision_recall_at_k(algo_knn_user)
```

    RMSE: 1.8455
    Precision: 1
    Recall: 0.941
    F1 score: 0.97


**Observations:**

- We can observe that the baseline model has RMSE=1.84 on the test set.
- Intuition of Recall - We are getting a recall of ~0.81, which means out of all the relevant books, 81% are recommended.
- Intuition of Precision - We are getting a precision of ~ 0.81, which means out of all the recommended books, 81% are relevant.
- Here F_1 score of the baseline model is ~0.81. It indicates that mostly recommended books were relevant and relevant books were recommended. We can try to improve the performance by using GridSearchCV to tune different hyperparameters of the algorithm.


```python
algo_knn_user.predict(1326, 12126, r_ui=8, verbose=True)
```

    user: 1326       item: 12126      r_ui = 8.00   est = 7.99   {'was_impossible': True, 'reason': 'User and/or item is unknown.'}





    Prediction(uid=1326, iid=12126, r_ui=8, est=7.9887628424657535, details={'was_impossible': True, 'reason': 'User and/or item is unknown.'})



- We can notice that this was a good prediction, as the predicted rating is 7.99 and original rating is 8.


```python
algo_knn_user.predict(1326, 2150, verbose=True)
```

    user: 1326       item: 2150       r_ui = None   est = 7.99   {'was_impossible': True, 'reason': 'User and/or item is unknown.'}





    Prediction(uid=1326, iid=2150, r_ui=None, est=7.9887628424657535, details={'was_impossible': True, 'reason': 'User and/or item is unknown.'})



**Fine tunning**
- We will be tuning hyperparameters for the KNNBasic algorithms


```python
# Setting up parameter grid to tune the hyperparameters
param_grid = {
    'k': [20, 30, 40],
    'min_k': [1,3,6],
    'sim_options': {
        'name': ['cosine', 'msd'],
        'user_based': [True]
    }
}
```


```python
# Performing 3-fold cross validation to tune the hyperparameters
gs = GridSearchCV(KNNBasic, param_grid, measures=['rmse', 'mae'], cv=3, n_jobs=1)

```


```python
# Fitting the data
gs.fit(data)
```

    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.



```python
# Obtaining bbest params
gs.best_params
```




    {'rmse': {'k': 20,
      'min_k': 6,
      'sim_options': {'name': 'msd', 'user_based': True}},
     'mae': {'k': 20,
      'min_k': 6,
      'sim_options': {'name': 'msd', 'user_based': True}}}




```python
gs.best_score
```




    {'rmse': 1.7007107538890953, 'mae': 1.3027997278856667}




```python
# Update our similarity options
sim_options = {
    'name': 'msd',
    'user_based': True
}
# Creating an instance of KNNBasic with optimal hyperparameter values
similarity_algo_optimized = KNNBasic(k=20, min_k=6, sim_options = sim_options, verbose = False)
```


```python
# Training the algorithm on the train set
similarity_algo_optimized.fit(trainset)
```




    <surprise.prediction_algorithms.knns.KNNBasic at 0x7b60476ba030>




```python
# Compute precision and recall
precision_recall_at_k(similarity_algo_optimized)
```

    RMSE: 1.6866
    Precision: 1
    Recall: 0.941
    F1 score: 0.97


**Observations:**

- After tuning hyperparameters, RMSE for the test set has reduced from 1.84 to 1.68.
- We can observe that after tuning the hyperparameters, the tuned model's F-1 score increased from 0.81 to 0.86 in comparison to the baseline model. As a result, we can say that the model's performance has improved after hyperparameter tuning.


```python
# Lets make predictions on an user and item
similarity_algo_optimized.predict(1326, 12344)
```




    Prediction(uid=1326, iid=12344, r_ui=None, est=7.9887628424657535, details={'was_impossible': True, 'reason': 'User and/or item is unknown.'})



**Observation:**

There is no difference in the prediction of the baseline model and the tuned model for this particular user-item pair. Both models predicted the rating as 7.99, which is very close to the actual rating of 8.


```python
# Lets try this on an item that the user has not rated
similarity_algo_optimized.predict(1326, 2150)
```




    Prediction(uid=1326, iid=2150, r_ui=None, est=7.9887628424657535, details={'was_impossible': True, 'reason': 'User and/or item is unknown.'})



We can find out the similar users to a given user or its nearest neighbors based on this KNNBasic algorithm. Below we are finding 5 most similar user to the user_id=1


```python
similarity_algo_optimized.get_neighbors(1, k=5)
```




    [7, 23, 95, 107, 109]




```python
# Lets create a function to obtain a top of recommended items
def get_recommendations(data, user_id, top_n, algo):

  # Creating an empty list to store the recommended book ids
  recommendations = []

  # Creating an user item interactions matrix
  user_item_interaction_matrix = data.pivot(index='user_id', columns='book_id', values='rating')

  # Extracting those book ids which the user_id has not interacted with yet
  non_interacted_items = user_item_interaction_matrix.loc[user_id][user_item_interaction_matrix.loc[user_id].isnull()].index.tolist()

  # Looping through each of the book id which user_id has not interacted with yet
  for book_id in non_interacted_items:

    # Predicting the ratings for those non interacted book ids by this user
    est = algo.predict(user_id, book_id).est

    # Appending the predicted ratings
    recommendations.append((book_id, est))

  # Sorting the predicted ratings in descending order
  recommendations.sort(key=lambda x: x[1], reverse=True)

  # Returning top n predicted rating items for this user
  return recommendations[:top_n]
```


```python
df_rating = df_rating.drop_duplicates()
df_rating
```





  <div id="df-0c52bc99-b29d-458c-834a-58c0205ed884" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>user_id</th>
      <th>book_id</th>
      <th>rating</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1211</th>
      <td>1251</td>
      <td>521</td>
      <td>9</td>
    </tr>
    <tr>
      <th>1213</th>
      <td>1251</td>
      <td>524</td>
      <td>9</td>
    </tr>
    <tr>
      <th>1214</th>
      <td>1251</td>
      <td>525</td>
      <td>8</td>
    </tr>
    <tr>
      <th>1456</th>
      <td>1252</td>
      <td>1</td>
      <td>10</td>
    </tr>
    <tr>
      <th>1474</th>
      <td>1252</td>
      <td>52</td>
      <td>9</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1149564</th>
      <td>1250</td>
      <td>928</td>
      <td>7</td>
    </tr>
    <tr>
      <th>1149581</th>
      <td>1250</td>
      <td>1288</td>
      <td>9</td>
    </tr>
    <tr>
      <th>1149592</th>
      <td>1250</td>
      <td>1316</td>
      <td>7</td>
    </tr>
    <tr>
      <th>1149627</th>
      <td>1250</td>
      <td>1483</td>
      <td>10</td>
    </tr>
    <tr>
      <th>1149637</th>
      <td>1250</td>
      <td>1496</td>
      <td>9</td>
    </tr>
  </tbody>
</table>
<p>26698 rows × 3 columns</p>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-0c52bc99-b29d-458c-834a-58c0205ed884')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-0c52bc99-b29d-458c-834a-58c0205ed884 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-0c52bc99-b29d-458c-834a-58c0205ed884');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-e936990c-a97a-4e5a-aa6a-63f4baa6d287">
      <button class="colab-df-quickchart" onclick="quickchart('df-e936990c-a97a-4e5a-aa6a-63f4baa6d287')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-e936990c-a97a-4e5a-aa6a-63f4baa6d287 button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

  <div id="id_bf744172-0c57-4aca-bb45-0d78c236041d">
    <style>
      .colab-df-generate {
        background-color: #E8F0FE;
        border: none;
        border-radius: 50%;
        cursor: pointer;
        display: none;
        fill: #1967D2;
        height: 32px;
        padding: 0 0 0 0;
        width: 32px;
      }

      .colab-df-generate:hover {
        background-color: #E2EBFA;
        box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
        fill: #174EA6;
      }

      [theme=dark] .colab-df-generate {
        background-color: #3B4455;
        fill: #D2E3FC;
      }

      [theme=dark] .colab-df-generate:hover {
        background-color: #434B5C;
        box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
        filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
        fill: #FFFFFF;
      }
    </style>
    <button class="colab-df-generate" onclick="generateWithVariable('df_rating')"
            title="Generate code using this dataframe."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M7,19H8.4L18.45,9,17,7.55,7,17.6ZM5,21V16.75L18.45,3.32a2,2,0,0,1,2.83,0l1.4,1.43a1.91,1.91,0,0,1,.58,1.4,1.91,1.91,0,0,1-.58,1.4L9.25,21ZM18.45,9,17,7.55Zm-12,3A5.31,5.31,0,0,0,4.9,8.1,5.31,5.31,0,0,0,1,6.5,5.31,5.31,0,0,0,4.9,4.9,5.31,5.31,0,0,0,6.5,1,5.31,5.31,0,0,0,8.1,4.9,5.31,5.31,0,0,0,12,6.5,5.46,5.46,0,0,0,6.5,12Z"/>
  </svg>
    </button>
    <script>
      (() => {
      const buttonEl =
        document.querySelector('#id_bf744172-0c57-4aca-bb45-0d78c236041d button.colab-df-generate');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      buttonEl.onclick = () => {
        google.colab.notebook.generateWithVariable('df_rating');
      }
      })();
    </script>
  </div>

    </div>
  </div>





```python
# Predicting the top 5 items for userId=1 using the similarity-based recommendation system
recommendations = get_recommendations(df_rating, 1, 5, similarity_algo_optimized)
recommendations
```




    [(259, 9.999999999999998),
     (1297, 9.88444587218763),
     (658, 9.870801662791411),
     (639, 9.764397905759163),
     (451, 9.702660811159905)]




```python
# Building the dataframe for above recommendations with columns "book_id" and "predicted_ratings"
pd.DataFrame(recommendations, columns=['book_id', 'rating'])
```





  <div id="df-f1ecb33e-5fab-434d-9243-fedb64c727cf" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>book_id</th>
      <th>rating</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>259</td>
      <td>10.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1297</td>
      <td>9.884446</td>
    </tr>
    <tr>
      <th>2</th>
      <td>658</td>
      <td>9.870802</td>
    </tr>
    <tr>
      <th>3</th>
      <td>639</td>
      <td>9.764398</td>
    </tr>
    <tr>
      <th>4</th>
      <td>451</td>
      <td>9.702661</td>
    </tr>
  </tbody>
</table>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-f1ecb33e-5fab-434d-9243-fedb64c727cf')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-f1ecb33e-5fab-434d-9243-fedb64c727cf button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-f1ecb33e-5fab-434d-9243-fedb64c727cf');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-1a1cb74d-c15f-4895-8cc4-fc8546df9b99">
      <button class="colab-df-quickchart" onclick="quickchart('df-1a1cb74d-c15f-4895-8cc4-fc8546df9b99')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-1a1cb74d-c15f-4895-8cc4-fc8546df9b99 button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

    </div>
  </div>




*Correcting the Ratings and Ranking the Books*

When comparing two books, it’s not enough to just look at their ratings — the number of people who rated each book also matters. A book with more ratings usually has a more reliable score. Because of this, we calculated a “corrected rating” for every book.

For example, a book with a rating of 8 but only 5 ratings is probably less trustworthy than a book rated 7 by 50 people. In general, the popularity or reliability of a book’s rating is related to the inverse of the square root of the number of ratings it has.


```python
def ranking_books(recommendations,final_rating):
  # Sort the books based on ratings count
  ranked_books = final_rating.loc[[items[0] for items in recommendations]].sort_values('rating_count', ascending=False)[['rating_count']].reset_index()
  # Merge with the recommended books to get predicted ratings
  ranked_books = ranked_books.merge(pd.DataFrame(recommendations, columns=['book_id', 'predicted_rating']), on='book_id', how='inner')
  # Rank the books based on corrected ratings
  ranked_books['corrected_ratings'] = ranked_books['predicted_rating'] - 1/np.sqrt(ranked_books['rating_count'])
  # Sort the books based on corrected ratings
  ranked_books = ranked_books.sort_values('corrected_ratings', ascending=False)
  return ranked_books
```


```python
recommendations
```




    [(259, 9.999999999999998),
     (1297, 9.88444587218763),
     (658, 9.870801662791411),
     (639, 9.764397905759163),
     (451, 9.702660811159905)]




```python
# Applying the ranking_books function and sorting it based on corrected ratings
ranking_books(recommendations, final_rating)
```





  <div id="df-6acbe924-17b4-4f3f-be57-2e69ffc0b497" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>book_id</th>
      <th>rating_count</th>
      <th>predicted_rating</th>
      <th>corrected_ratings</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>3</th>
      <td>259</td>
      <td>31</td>
      <td>10.000000</td>
      <td>9.820395</td>
    </tr>
    <tr>
      <th>0</th>
      <td>658</td>
      <td>53</td>
      <td>9.870802</td>
      <td>9.733441</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1297</td>
      <td>35</td>
      <td>9.884446</td>
      <td>9.715415</td>
    </tr>
    <tr>
      <th>1</th>
      <td>639</td>
      <td>43</td>
      <td>9.764398</td>
      <td>9.611899</td>
    </tr>
    <tr>
      <th>4</th>
      <td>451</td>
      <td>18</td>
      <td>9.702661</td>
      <td>9.466959</td>
    </tr>
  </tbody>
</table>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-6acbe924-17b4-4f3f-be57-2e69ffc0b497')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-6acbe924-17b4-4f3f-be57-2e69ffc0b497 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-6acbe924-17b4-4f3f-be57-2e69ffc0b497');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-1f2aefff-bdfc-4724-a2e5-6ff47d224852">
      <button class="colab-df-quickchart" onclick="quickchart('df-1f2aefff-bdfc-4724-a2e5-6ff47d224852')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-1f2aefff-bdfc-4724-a2e5-6ff47d224852 button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

    </div>
  </div>




**Model 3: Item based Collaborative Filtering Recommendation System**


We have seen user-user similarity-based collaborative filtering. Now, let us look into similarity-based collaborative filtering where similarity is calculated between items.


```python
# Defining item similarity measure
sim_options = {
    'name': 'cosine',
    'user_based': False
}
```


```python
# Defining nearest neighbour algorithm
algo_knn_item = KNNBasic(sim_options=sim_options)
# Train the algorithm on the train set
algo_knn_item.fit(trainset)
```

    Computing the cosine similarity matrix...
    Done computing similarity matrix.





    <surprise.prediction_algorithms.knns.KNNBasic at 0x7b6047533f50>




```python
# Compute recal and precision
precision_recall_at_k(algo_knn_item)
```

    RMSE: 1.6210
    Precision: 1
    Recall: 0.941
    F1 score: 0.97


**Observations:**

We can observe that the baseline model has RMSE=1.62 & F_1 Score=0.80on the test set.
We can try to improve the performance number by using GridSearchCV to tune different hyperparameters of this algorithm.


```python
# Predict an item on a given user
algo_knn_item.predict(1326, 12344)
```




    Prediction(uid=1326, iid=12344, r_ui=None, est=7.9887628424657535, details={'was_impossible': True, 'reason': 'User and/or item is unknown.'})




```python
algo_knn_item.predict(1326, 2150)
```




    Prediction(uid=1326, iid=2150, r_ui=None, est=7.9887628424657535, details={'was_impossible': True, 'reason': 'User and/or item is unknown.'})




```python
# Setting up parameter grid to tune the hyperparameters
param_grid = {
    'k': [10, 20, 30],
    'min_k': [3,6,9],
    'sim_options': {
        'name': ['msd', 'cosine'],
        'user_based': [False]
    }
}
```


```python
# Setting up parameter grid to tune the hyperparameters
grib_obj = GridSearchCV(KNNBasic, param_grid, measures=['rmse'], cv=3)

# Fitting the data
grib_obj.fit(data)
```

    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the msd similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    Computing the cosine similarity matrix...
    Done computing similarity matrix.



```python
# Obtaining the best score
grib_obj.best_score
```




    {'rmse': 1.594003880621386}




```python
# Obtaining best parameters
grib_obj.best_params
```




    {'rmse': {'k': 30,
      'min_k': 3,
      'sim_options': {'name': 'cosine', 'user_based': False}}}




```python
# Creating an instance of KNNBasic with optimal hyperparameter values
similarity_algo_optimized_item = KNNBasic(k=30, min_k=3, sim_options = {'name': 'cosine', 'user_based': False})
```


```python
# Training the algorithm on the train set
similarity_algo_optimized_item.fit(trainset)

# Compute precison and recall
precision_recall_at_k(similarity_algo_optimized_item)
```

    Computing the cosine similarity matrix...
    Done computing similarity matrix.
    RMSE: 1.5882
    Precision: 1
    Recall: 0.941
    F1 score: 0.97


**Observations:**

We observe that after tuning hyperparameters, RMSE for the test set has reduced to 1.58 from 1.62. F_1 score of the tuned model is also slightly better than the baseline model. So, the model performance has improved slightly after hyperparameter tuning.


```python
# Predictions for known item
similarity_algo_optimized_item.predict(1326, 12344)
```




    Prediction(uid=1326, iid=12344, r_ui=None, est=7.9887628424657535, details={'was_impossible': True, 'reason': 'User and/or item is unknown.'})




```python
similarity_algo_optimized_item.predict(1326, 2150)
```




    Prediction(uid=1326, iid=2150, r_ui=None, est=7.9887628424657535, details={'was_impossible': True, 'reason': 'User and/or item is unknown.'})




```python
# Identifying neighbors
similarity_algo_optimized_item.get_neighbors(1, k=5)
```




    [11, 12, 17, 21, 22]




```python
# Predict top 5 books
recommendations = get_recommendations(df_rating, 1, 5, similarity_algo_optimized_item)
# Building the dataframe for above recommendations with columns "book_id" and "predicted_ratings"
pd.DataFrame(recommendations, columns=['book_id', 'predicted_ratings'])
```





  <div id="df-c9e3f25f-0645-4fda-8994-1b4f089ed612" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>book_id</th>
      <th>predicted_ratings</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>10</td>
    </tr>
    <tr>
      <th>1</th>
      <td>15</td>
      <td>10</td>
    </tr>
    <tr>
      <th>2</th>
      <td>16</td>
      <td>10</td>
    </tr>
    <tr>
      <th>3</th>
      <td>17</td>
      <td>10</td>
    </tr>
    <tr>
      <th>4</th>
      <td>30</td>
      <td>10</td>
    </tr>
  </tbody>
</table>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-c9e3f25f-0645-4fda-8994-1b4f089ed612')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-c9e3f25f-0645-4fda-8994-1b4f089ed612 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-c9e3f25f-0645-4fda-8994-1b4f089ed612');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-dbe2d01f-657a-4d33-aeee-f7d6f767ac77">
      <button class="colab-df-quickchart" onclick="quickchart('df-dbe2d01f-657a-4d33-aeee-f7d6f767ac77')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-dbe2d01f-657a-4d33-aeee-f7d6f767ac77 button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

    </div>
  </div>





```python
# Applying the ranking_books function and sorting it based on corrected ratings
ranking_books(recommendations, final_rating)
```





  <div id="df-72da6b1c-ecc8-4d48-ae0f-08963f7df51b" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>book_id</th>
      <th>rating_count</th>
      <th>predicted_rating</th>
      <th>corrected_ratings</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>28</td>
      <td>10</td>
      <td>9.811018</td>
    </tr>
    <tr>
      <th>1</th>
      <td>15</td>
      <td>13</td>
      <td>10</td>
      <td>9.722650</td>
    </tr>
    <tr>
      <th>2</th>
      <td>16</td>
      <td>13</td>
      <td>10</td>
      <td>9.722650</td>
    </tr>
    <tr>
      <th>3</th>
      <td>17</td>
      <td>12</td>
      <td>10</td>
      <td>9.711325</td>
    </tr>
    <tr>
      <th>4</th>
      <td>30</td>
      <td>10</td>
      <td>10</td>
      <td>9.683772</td>
    </tr>
  </tbody>
</table>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-72da6b1c-ecc8-4d48-ae0f-08963f7df51b')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-72da6b1c-ecc8-4d48-ae0f-08963f7df51b button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-72da6b1c-ecc8-4d48-ae0f-08963f7df51b');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-58e4c8c4-dd48-4dc0-a582-b5072b48f497">
      <button class="colab-df-quickchart" onclick="quickchart('df-58e4c8c4-dd48-4dc0-a582-b5072b48f497')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-58e4c8c4-dd48-4dc0-a582-b5072b48f497 button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

    </div>
  </div>




**Model 4: Matrix Factorization**

Model-based Collaborative Filtering is a personalized recommendation system. The recommendations are based on the past behavior of the user and it is not dependent on any additional information. We use latent features to find recommendations for each user.


**Singular Value Decomposition (SVD)**
SVD is used to compute the latent features from the user-item matrix that we already learned earlier. But SVD does not work when we miss values in the user-item matrix.


```python
# Using SVD matrix factorization
svd = SVD(random_state = 1)
# Training the algorithm on the train set
svd.fit(trainset)
```




    <surprise.prediction_algorithms.matrix_factorization.SVD at 0x7b603cd81b50>




```python
# Compute precision and recall
precision_recall_at_k(svd)
```

    RMSE: 1.5106
    Precision: 1
    Recall: 0.941
    F1 score: 0.97


**Observations:**

We observe that the baseline F_1 score for the matrix factorization model on the test set is higher in comparison to the F_1 score for the user-user similarity-based recommendation system and lower in comparison to the optimized user-user similarity-based recommendation system.
The result for SVD is better than both baseline and optimized item-item similarity-based recommendation systems.


```python
# Predict for known user
svd.predict(1326, 12344)
```




    Prediction(uid=1326, iid=12344, r_ui=None, est=7.9887628424657535, details={'was_impossible': False})




```python
svd.predict(1326, 2150)
```




    Prediction(uid=1326, iid=2150, r_ui=None, est=7.9887628424657535, details={'was_impossible': False})




```python
# Tune hyper parameters
param_grid = {
    'n_epochs': [10, 20, 30],
    'lr_all': [0.001, 0.005, 0.01],
    'reg_all': [0.2, 0.4, 0.6]
    }
```


```python
# Performing 3-fold gridsearch cross validation
gs_ = GridSearchCV(SVD, param_grid, measures=['rmse'], cv=3, n_jobs=1)
# Fitting data
gs_.fit(data)
```


```python
# Obtaining best parameters
gs_.best_params
```




    {'rmse': {'n_epochs': 20, 'lr_all': 0.01, 'reg_all': 0.2}}



Now, let's build the final model by using optimal values of the hyperparameters which we received by using grid search cross-validation.


```python
# Building the optimized SVD model
svd_optimized = SVD(n_epochs=20, lr_all=0.01, reg_all=0.2, random_state = 1)
# Training the algorithm on the train set
svd_optimized.fit(trainset)
```




    <surprise.prediction_algorithms.matrix_factorization.SVD at 0x7b603cd81910>




```python
# compute precision and recall
precision_recall_at_k(svd_optimized)
```

    RMSE: 1.5026
    Precision: 1
    Recall: 0.941
    F1 score: 0.97


**Observation:**

We observe that after tuning hyperparameters, the model performance has not improved by much. We can try other values for hyperparameters and see if we can get a better performance. However, here we will proceed with the existing model.


```python
# Predict for a known user
svd_optimized.predict(1326, 12344)
```




    Prediction(uid=1326, iid=12344, r_ui=None, est=7.9887628424657535, details={'was_impossible': False})




```python
svd_optimized.predict(1326, 2150)
```




    Prediction(uid=1326, iid=2150, r_ui=None, est=7.9887628424657535, details={'was_impossible': False})




```python
# Getting top 5 recommendations for user_id 1 using "svd_optimized" algorithm
svd_recommendations = get_recommendations(df_rating, 1, 5, svd_optimized)
```


```python
# Ranking book based on above recommendations
ranking_books(svd_recommendations, final_rating)
```





  <div id="df-c7614d01-6a74-4018-b4de-7d9653463731" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>book_id</th>
      <th>rating_count</th>
      <th>predicted_rating</th>
      <th>corrected_ratings</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>70</td>
      <td>32</td>
      <td>10</td>
      <td>9.823223</td>
    </tr>
    <tr>
      <th>1</th>
      <td>65</td>
      <td>15</td>
      <td>10</td>
      <td>9.741801</td>
    </tr>
    <tr>
      <th>2</th>
      <td>16</td>
      <td>13</td>
      <td>10</td>
      <td>9.722650</td>
    </tr>
    <tr>
      <th>3</th>
      <td>17</td>
      <td>12</td>
      <td>10</td>
      <td>9.711325</td>
    </tr>
    <tr>
      <th>4</th>
      <td>34</td>
      <td>12</td>
      <td>10</td>
      <td>9.711325</td>
    </tr>
  </tbody>
</table>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-c7614d01-6a74-4018-b4de-7d9653463731')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-c7614d01-6a74-4018-b4de-7d9653463731 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-c7614d01-6a74-4018-b4de-7d9653463731');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-14f7e496-3f4d-473c-9329-7f3f27ee743a">
      <button class="colab-df-quickchart" onclick="quickchart('df-14f7e496-3f4d-473c-9329-7f3f27ee743a')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-14f7e496-3f4d-473c-9329-7f3f27ee743a button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

    </div>
  </div>




**Conclusion**

In this case study, we built recommendation systems using four different algorithms. They are as follows:

- Rank-based using averages
- User-user similarity-based collaborative filtering
- Item-item similarity-based collaborative filtering
- Model-based (matrix factorization) collaborative filtering

To demonstrate "user-user similarity-based collaborative filtering", "item-item similarity-based collaborative filtering", and "model-based (matrix factorization) collaborative filtering", surprise library has been used. For these algorithms, grid search cross-validation is used to find the optimal hyperparameters for the data, and improve the performance of the model**.

For performance evaluation of these models, precision@k and recall@k are used. Using these two metrics, the F_1 score is calculated for each working model.

Overall, the optimized user-user similarity-based recommendation system has given the best performance in terms of the F1-Score (~0.86)

Collaborative Filtering searches for neighbors based on similarity of books (example) preferences and recommend books that those neighbors read while Matrix factorization works by decomposing the user-item matrix into the product of two lower dimensionality rectangular matrices.

Matrix Factorization has lower RMSE (1.50) due to the reason that it assumes that both books and users are present in some low dimensional space describing their properties and recommend a book based on its proximity to the user in the latent space. Implying it accounts for latent factors as well.

We can try to further improve the performance of these models using hyperparameter tuning.

We can also try to combine different recommendation techniques to build a more complex model like hybrid recommendation systems.
