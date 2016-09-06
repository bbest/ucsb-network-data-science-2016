---
layout: default
---

- [Day 02: Data Science, Git/Github, Python Basics, Python for Graphs and Tables](https://github.com/bbest/ucsb-network-data-science-2016/blob/gh-pages/day02b_python.ipynb)

# Github Directory for UCSB Network Data Science Boot Camp ({{ site.current_term }})

{% include students.html %}

<br>
<br>
<br>
<br>
<br>
<br>

## Add yourself

Introduce yourself via a `GITHUB_USERNAME.json` file under the [`_data/{{ site.current_term }}/`](https://github.com/{{ site.git_owner }}/{{ site.git_repo }}/tree/gh-pages/_data/{{ site.current_term }}) directory, and submit via [pull request](https://help.github.com/articles/creating-a-pull-request/). Remember to first [fork](https://help.github.com/articles/fork-a-repo/) your own copy of the repository [{{ site.git_owner }}/{{ site.git_repo }}](https://github.com/{{ site.git_owner }}/{{ site.git_repo }}) so that you can write the file to the repo before submitting the pull request.

Here's an example file at [`_data/{{ site.current_term }}/bbest.json`](https://github.com/{{ site.git_owner }}/{{ site.git_repo }}/tree/gh-pages/_data/{{ site.current_term }}/bbest.json)

```javascript
{
	"department": "MSI, NCEAS (consultant)",
	"interests": "marine biodiversity, ocean health",
	"project": "",
	"project_url": ""
}
```

Using the format above, replace with your own `department` and `interests`. We'll update `project` and `project_url` later once you've decided on a project and have a project URL.

## Details

The details of how this works (using [Jekyll data files](https://jekyllrb.com/docs/datafiles/)) are beyond the scope of this boot camp, but provides a simple satisfying example for applying the fork & pull request model to a repository for which you do not have write permissions and want to contribute towards.

This technique is borrowed from [advanced-js/students](https://github.com/advanced-js/students): "student directory, for practicing doing pull requests".
