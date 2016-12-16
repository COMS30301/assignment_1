# Assignment 1: ML workflow with scikit-learn
## Description
In this lab you will have a chance to develop a machine learning pipeline that recognises hand-written digits. The dataset that you will use for this assignment is [MNIST](http://yann.lecun.com/exdb/mnist/): 27x27 pixels grayscale images.  
In this assignment you are asked to pick any 2 digits: `0, 1, 2, 3, 4, 5, 6, 7, 8, 9`, from the MNIST dataset (500 random samples per chosen digit). Then extract any 2 selected features from the ones prepared for you: `f1, f2, f3, f4, f5, f6, f7, f8, f9`.

Once you have prepared the dataset you need to choose a machine learning algorithm from `scikit-learn` and apply it. You need to decide how to evaluate your results (cross-validation, training-test split, etc.), what performance metric to use and how to report your results. Motivate all your choices.

To get you started you are given the dataset loader and two functions:
* `pick_digits`, and
* `pick_features`;

together with and an example how to use them.

One thing you might want to do is to plot the decision boundaries. Lab3 showed how to do this for a linear classifier, but for other classifiers this can be a bit more involved. One way to visualise decision regions is to colour-code the predictions of the classifier over a mesh grid (see [link](http://scikit-learn.org/stable/auto_examples/neighbors/plot_classification.html#sphx-glr-auto-examples-neighbors-plot-classification-py) to NearestNeighbors in scikit-learn). Another possibility is to calculate posterior class probabilities over a mesh grid and draw a contour line at p=1/2 (see [link](http://matplotlib.org/examples/pylab_examples/contour_demo.html) to matplotlib contour demo).

## Marking criteria
* 30% - develop one working solution;
* 10% - support it with relevant plots and figures eg. data scatter plot with decision boundary, predictive accuracy;

---

* 20% - develop another working solution of different type;
* 10% - support it with relevant plots and figures eg. data scatter plot with decision boundary, predictive accuracy;

---

* 10% - motivate your choices (5% per solution);
* 10% - create a baseline for your dataset;
* 10% - compare your results against each other (5%) and the baseline (5%).

---

Please put all your working and comments in this Jupyter notebook and submit it as **the only** file with name `<your_candidate_number>.ipynb` eg. `12321.ipynb`. If you do not use this naming convention **10%** will be subtracted from your mark!  
Your candidate number can be found on your [FEN](https://wwwa.fen.bris.ac.uk/coms/index.jsp) **profile** next to *Candidate:* keyword.

## Requirements
### Python version
This coursework must be completed using `Python 2.x.x`. If you have troubles running Python on any of the MVB 2.11 lab machines please execute the following command first:
```
export PATH=/opt/anaconda/python2/bin:$PATH
```

All submissions that use `Python 3.x.x` will be given 0 marks.

### Running the code on Windows
If you want to run the notebook on Windows machine you need to replace the line:
```
mnist = fetch_mldata('MNIST original')
```

with:
```
mnist = fetch_mldata('MNIST original', data_home='***')
```

where `***` should be replaced with location where the dataset will be stored.

**Before submission please make sure that the code runs on MVB 2.11 lab machines!** If it doesn't you will be given 0 marks.
