# ucsb-network-data-science-2016

UCSB IGERT Network Data Science Boot Camp (2016) materials

This is initially just my portion of the boot camp for setup and 2 hours of initial instruction.

## Setup

Optional in brackets:

- Python: Anaconda distribution
  - IDE: [Rodeo](https://www.yhat.com/products/rodeo) like RStudio
- [R, Rstudio]
- Git, Github. [GitKraken]

## Git, Github

- git vs github
- Github Features
  - technical convo: commits, pull requests, line # links
  - rendered & diff formats: md, csv, geojson
  - project mgt: linking b/n issues, milestones & commits
- Exercises:
  - setup Github account
  - Exercise for git: clone, add (json for class directory), commit, push, pull request
- [Github Pages, Markdown, Rmarkdown, presentation, website]

## Python

Have notes, but do interactively

- Python console, basic calculator
- Jupyter Notebook
- everything is an object: `dir`
  - modules
- whitespace matters: loops, conditionals
- data types: 
  - number (divide int vs float)
  - strings: real vs unicode
  - lists. list comprehension
  - dictionaries
  - [Python Advanced: Graph Theory and Graphs in Python](http://www.python-course.eu/graphs_python.php)
  - Graph in NetworkX: [networkx/graph.py at master · networkx/networkx](https://github.com/networkx/networkx/blob/master/networkx/classes/graph.py#L181-L185):
  
    > The Graph class uses a dict-of-dict-of-dict data structure.
    The outer dict (node_dict) holds adjacency information keyed by node.
    The next dict (adjlist_dict) represents the adjacency information and holds
    edge data keyed by neighbor.  The inner dict (edge_attr_dict) represents
    the edge data and holds edge attribute values keyed by attribute names.
  - dates. import modules
  
    - [Creating a graph — NetworkX 1.11 documentation](http://networkx.readthedocs.io/en/networkx-1.11/tutorial/tutorial.html)
  
    - [Graphs and networks¶](http://www.simondobson.org/complex-networks-complex-processes/concepts-networks.html) (github: [simoninireland/cncp](https://github.com/simoninireland/cncp): complex networks, complex processes)

## PANDAS

Tabular data (esp CSV)

- [csv — CSV File Reading and Writing — examples](https://docs.python.org/3/library/csv.html#examples)

  - TODO: represent each row with own key,val vs each col has key: list of values

  ```python
import csv

d = {}
rdr = csv.reader(open('filename.csv', 'r'))
d.keys = rdr.next()
for row in rdr:
   k, v = row
   d[d.keys()] = v
```
-[pandas](http://pandas.pydata.org/pandas-docs/stable/) is well suited for "Tabular data with heterogeneously-typed columns, as in an SQL table or Excel spreadsheet"
- [Package overview — pandas 0.18.1 documentation](http://pandas.pydata.org/pandas-docs/stable/overview.html)
- [10 Minutes to pandas — pandas 0.18.1 documentation](http://pandas.pydata.org/pandas-docs/stable/10min.html)
- read csv (vs dic representation)
  ```python
  dic = pd.Series.from_csv(filename, names=cols, header=None).to_dict()
  ```
- data frames
- [12 Useful Pandas Techniques in Python for Data Manipulation](https://www.analyticsvidhya.com/blog/2016/01/12-pandas-techniques-python-data-manipulation/)

# Projects

Both projects rely on creation of simpler networks from a dense raster for various applications:

- assessing spatial connectivity of habitats (Python)
  - extract TIN with cumulative distance away from patches for determining distances away
  - Keitt & Urban, Urban et al
  
- ship routing applications to avoid whale strikes (R)
  - increase density closer to shore

- how to make sparse networks from:
  - dens
