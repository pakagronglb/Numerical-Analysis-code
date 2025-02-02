<a name="readme-top"></a>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/almsam/Numerical-Analysis-code.git">
    <img src="https://github.com/almsam/Numerical-Analysis-code/blob/main/images/PF logo.png" alt="Logo" width="270" height="270">
  </a>

<h1 align="center">Numerically Analyzing my Data</h1>

<p align="center">
  <strong>Mission Statement</strong><br>
  "My mission is to implement various mathematical algorithms in Python for practice, to test my skills, to document the methods, and just for fun"
</p>

<p align="center">
  <strong>Project Summary</strong><br>
  During my third year of post secondary, I learnt a ton of algorithms for solving problems in my numerical analysis course, however I have only implemented them in MATLAB thus-far. Hence: my goal here is to implement algorithms - including but not limited to Newtons Method, the Bisection Method, Lagrange Interpolation, Trapezoid & Simpsons Integration, & Lipchitz Algorithm, as well as Euler's & Heun's Methods for approximating ODE's - in Python. Also Just for fun im going to sprinkle in some of my own creations i've wanted for a while - such as using multiple regression techniques to find the best fit function on a dataset.
</p>

</div>

<!-- ABOUT THE PROJECT -->
## About The Project

### Built By [Samira](https://github.com/almsam) With: [![Py][Py]][PyUrl] using [![Numpy][Numpy]][Numpy-url][![Pandas][Pandas]][Pandas-url][![Matplotlib][Matplotlib]][Matplotlib-url][![Statsmodels][Statsmodels]][Statsmodels-url] &[![SymPy][SymPy]][SymPy-url]

[Py]: https://img.shields.io/badge/Python%20-%20%233e50b5?logo=python&logoColor=%23FFDE57&logoSize=auto
[PyUrl]: https://www.python.org

[Numpy]: https://img.shields.io/badge/NumPy-%20%23013243?logo=numpy&logoColor=%23FFFFFF&logoSize=auto
[Numpy-url]: https://numpy.org/
[Matplotlib]: https://img.shields.io/badge/MatPlotLib-%20%2345ca9a?logo=python&logoColor=%23FFFFFF&logoSize=auto
[Matplotlib-url]: https://matplotlib.org/
[Seaborn]: https://img.shields.io/badge/SeaBorn-%20%2365baea?logo=python&logoColor=%23FFFFFF&logoSize=auto
[Seaborn-url]: https://seaborn.pydata.org/
[Pandas]: https://img.shields.io/badge/Pandas%20-%20%23150458?logo=pandas&logoColor=%23FFFFFF&logoSize=auto
[Pandas-url]: https://pandas.pydata.org/
[Statsmodels]: https://img.shields.io/badge/StatsModels%20-%20%231e3095?logo=python&logoColor=%23FFFFFF&logoSize=auto
[Statsmodels-url]: https://www.statsmodels.org/stable/index.html
[Flask]: https://img.shields.io/badge/Flask%20-%20%23000000?logo=flask&logoColor=%23FFFFFF&logoSize=auto
[Flask-Url]: https://flask.palletsprojects.com/en/3.0.x/
[Scikit-learn]: https://img.shields.io/badge/SciKit%20Learn%20-%20%2344a9dd?logo=scikitlearn&logoColor=%23FFFFFF&logoSize=auto
[Scikit-learn-url]: https://scikit-learn.org/stable/
[SymPy]: https://img.shields.io/badge/SymPy%20-%20%233B5526?logo=sympy&logoColor=%23FFFFFF&logoSize=auto
[SymPy-url]: https://www.sympy.org/en/index.html

<!-- FEATURES -->
## Project Features

### Plot Finder
- After completing a lab in 1st year physics to derive a formula for a tenis balls flight by collecting data in a video, I realzied the lack of frameworks in place to detrmine the relationship between variables
- Enter Plot Finder: [Plot_Finder.py](https://github.com/almsam/Numerical-Analysis-code/blob/main/Plot_Finder.py) runs a linear, quadratic, cubic, higher polynomial, exponential, logarithmic, Loess, & sinosudial regressions, then using the smallest error case to determine the best guess for the best fit line of the graph
- The next Iteration of development was to return the function of the line of best fit after finding both the function and the parameters of correlation that minimize error
- And the current Iteration after that involves Forior series regression by computing a best fit function as multiple functions summed together (which can be done by regressing on the error terms) - which theoretically could mean the error of a graph could be chocked up to a sinosudial term in the true function

  The Goal here? I would like to ultimately bridge this section of the project into an open source library/package to serve as an aditional tool in our workforces data science toolboxes

### How do I use Plot Finder?

First, install the dependecies:

```
pip install numpy pandas seaborn matplotlib statsmodels sympy
```

Next, prepare your data with an independent & dependent variabke: example CSV:

```
age, length
15, 5.1
16, 5.3
17, 5.6
```

Then you can run the script:

Save the script (Plot_Finder.py) to your local machine, & append this to a Python file's import section

```
from Plot_Finder import find_best_fit
import pandas as pd
```

& finally, run ```find_best_fit(x, y)``` on your data, Plot Finder will provide a similar output to:

```
--- Regression Errors ---
Linear Error: 2.5064127927953335  
Quadratic Error: 2.376293313469839
Cubic Error: 2.3306552613010023
Exponential Error: 2.5033863710624638
Logarithmic Error: 2.408240048405719
Sine Error: 2.5278577442576977
LOESS Error: 3.5317500644855344
Polynomial (x^4) Error: 2.3629127943906134
Polynomial (x^5) Error: 2.3953673780927542
Polynomial (x^6) Error: 2.357742781477933
Polynomial (x^7) Error: 2.3560983113517175

The method with the smallest error is: Cubic Regression with an error of 2.3306552613010023

Approximate function: 0.0436070723456402*x**3 - 0.787115855407833*x**2 + 4.5685444988691*x + 85.1575254621457

plotting: 0.0436070723456402*x**3 - 0.787115855407833*x**2 + 4.5685444988691*x + 85.1575254621457
```

and give you a plot to vizualize the data & regression line provided, 

<!-- IMPROVEMENTS -->
## Future Improvements

this project aims to be expanded into an open-source library with additional features, including:
- Support for more regression methods.
- Option to handle multivariate datasets (more than one independent variable).
- Enhanced error metrics for model selection (e.g., R², Adjusted R²).
- Optimization options for fine-tuning parameters such as the LOESS frac value.

<!-- Contribution -->
## Contribution

Contributions to improve the script or add new features are welcome! Feel free to fork the repository and submit pull requests.
