### Installing `alns`

The `alns` package depends on `numpy` and `matplotlib`. It may be installed in the
usual way as
```
git clone https://github.com/ss48/ALNS.git
run the following scripts:
python3 Trav_SalMan.py
or
python3 Trav_SalMan1.py
```
Additionally, to enable more advanced operator selection schemes using 
multi-armed bandit algorithms, `alns` may be installed with the optional 
[MABWiser][12] dependency:
```
pip install alns[mabwiser]
```

### Getting started

The documentation is available [here][1]. If you are new to metaheuristics or 
ALNS, you might benefit from reading the [introduction to ALNS][11] page.

The `alns` library provides the ALNS algorithm and various acceptance criteria,
operator selection schemes, and stopping criteria. To solve your own problem,
you should provide the following:

- A solution state for your problem that implements an `objective()` function.
- An initial solution.
- One or more destroy and repair operators tailored to your problem.

A "quickstart" code template is available [here][10].

### Examples

We provide several example notebooks showing how the ALNS library may be used.
These include:

- The travelling salesman problem (TSP), [here][2]. We solve an instance of 131
  cities using very simple destroy and repair heuristics.
- The capacitated vehicle routing problem (CVRP), [here][8]. We solve an
  instance with 241 customers using a combination of a greedy repair operator,
  and a _slack-induced substring removal_ destroy operator.
- The cutting-stock problem (CSP), [here][4]. We solve an instance with 180
  beams over 165 distinct sizes in only a very limited number of iterations.
- The resource-constrained project scheduling problem (RCPSP), [here][6]. We
  solve an instance with 90 jobs and 4 resources using a number of different
  operators and enhancement techniques from the literature.
- The permutation flow shop problem (PFSP), [here][9]. We solve an instance with
  50 jobs and 20 machines. Moreover, we demonstrate multiple advanced features
  of ALNS, including auto-fitting the acceptance criterion and adding local
  search to repair operators. We also demonstrate how one could tune ALNS
  parameters.

Finally, the features notebook gives an overview of various options available in
the `alns` package. In the notebook we use these different options to solve a
toy 0/1-knapsack problem. The notebook is a good starting point for when you
want to use different schemes, acceptance or stopping criteria yourself. It is
available [here][5].

### Contributing

We are very grateful for any contributions you are willing to make. Please have
a look [here][3] to get started. If you aim to make a large change, it is
helpful to discuss the change first in a new GitHub issue. Feel free to open
one!

### Getting help

If you are looking for help, please follow the instructions [here][7].

### How to cite `alns`

If you use `alns` in your research, please consider citing the following paper:

> Wouda, N.A., and L. Lan (2023). 
> ALNS: a Python implementation of the adaptive large neighbourhood search metaheuristic. 
> _Journal of Open Source Software_, 8(81): 5028. 
> https://doi.org/10.21105/joss.05028

Or, using the following BibTeX entry:

```bibtex
@article{Wouda_Lan_ALNS_2023, 
  doi = {10.21105/joss.05028}, 
  url = {https://doi.org/10.21105/joss.05028}, 
  year = {2023}, 
  publisher = {The Open Journal}, 
  volume = {8}, 
  number = {81}, 
  pages = {5028}, 
  author = {Niels A. Wouda and Leon Lan}, 
  title = {{ALNS}: a {P}ython implementation of the adaptive large neighbourhood search metaheuristic}, 
  journal = {Journal of Open Source Software} 
}
```

[1]: https://alns.readthedocs.io/en/latest/

[2]: https://alns.readthedocs.io/en/latest/examples/travelling_salesman_problem.html

[3]: https://alns.readthedocs.io/en/latest/setup/contributing.html

[4]: https://alns.readthedocs.io/en/latest/examples/cutting_stock_problem.html

[5]: https://alns.readthedocs.io/en/latest/examples/alns_features.html

[6]: https://alns.readthedocs.io/en/latest/examples/resource_constrained_project_scheduling_problem.html

[7]: https://alns.readthedocs.io/en/latest/setup/getting_help.html

[8]: https://alns.readthedocs.io/en/latest/examples/capacitated_vehicle_routing_problem.html

[9]: https://alns.readthedocs.io/en/latest/examples/permutation_flow_shop_problem.html

[10]: https://alns.readthedocs.io/en/latest/setup/template.html

[11]: https://alns.readthedocs.io/en/latest/setup/introduction_to_alns.html

[12]: https://github.com/fidelity/mabwiser
