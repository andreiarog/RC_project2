# RC_project2

Network Science Project 2: Overall description of brain network mapped by Crossley et al. (2013). Application and evaluation of several algorithms used in community detection, and their interceptions with respective anatomical labels (obtained through label4MRI tool).

Jupyter Files:
- proj_initial_analysis: degree distribution, clustering, centrality and small-world properties analysis
- proj_main_analysis: communities study
- 3D visualization of brain with nodes colored according to their communities
	- brain_visualization - Louvain 
	- brain_visualization - Newman
	- brain_visualization - Real

Summary of imports of libraries:

- General
import networkx as nx
import numpy as np
import pandas as pd
import community
from networkx.algorithms.link_analysis import hits
import igraph as ig
from igraph import *

- Matplot
import matplotlib.path as mpath
import matplotlib.pyplot as plt
from matplotlib.lines import Line2D

- Require installation
import rpy2.robjects as robjects
from rpy2.robjects import numpy2ri
>> conda install -c r rpy2 

- Additional Library in project folder
import sys
sys.path.append('python-modularity-maximization')
from modularity_maximization import partition
from modularity_maximization.utils import get_modularity

- Visualization package
import plotly
import plotly.plotly as py
import plotly.graph_objs as go

#Requires sign-in in package portal and creation of key
plotly.tools.set_credentials_file(username='andreiarog', api_key='4QtzshXlWo5mEnzFA7zo')

- Others
from operator import itemgetter
import collections
import scipy.io
import itertools
from itertools import product
from random import shuffle
from numpy import sort

