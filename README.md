# DiscoDNC

Deterministic Network Calculus (DNC) is a methodology for worst-case modeling and analysis of communication networks. It enables to derive deterministic bounds on a server’s backlog as well as a flow’s end-to-end delay. Given a directed graph of servers (server graph) and the flows crossing these servers, the Disco Deterministic Network Calculator (DiscoDNC) automates the derivation of bounds.

<<<<<<< HEAD

### Academic Attribution

If you use the Disco Deterministic Network Calculator for research, please include the following reference in any resulting publication:

```plain
@inproceedings{DiscoDNCv2,
  author    = {Steffen Bondorf and Jens B. Schmitt},
  title     = {The {DiscoDNC} v2 -- A Comprehensive Tool for Deterministic Network Calculus},
  booktitle = {Proc. of the International Conference on Performance Evaluation Methodologies and Tools},
  series    = {ValueTools '14},
  pages     = {44--49},
  month     = {December},
  year      = 2014,
  url       = {https://dl.acm.org/citation.cfm?id=2747659}
}
```
=======
# Submodule structure

* combine profiles as needed
The DiscoDNC code consists of 4 parts, that are structured in 4 different repositories. The base code in `src/main` is contained in this repository, where the ones are included as submodules as follows. The MPARTC wrapper in `src/mpa_ext` is located in [DiscoDNCext_MPARTC](https://github.com/NetCal/DiscoDNCext_MPARTC), the test files in `src/test` are in [DiscoDNC_tests](https://github.com/NetCal/DiscoDNC_tests) and the experiment extension in `src/experiments` are in [DiscoDNC_experiments](https://github.com/NetCal/DiscoDNC_experiments). In order to checkout the submodules 

# Compile jars

Use the following maven profiles for compiling jars the different parts of the DiscoDNC

* `mvn package` - builds the base code in `src/main`
* `mvn package -P mpa` - builds the base code and the MPARTC wrappers in `src/mpa_ext`
* `mvn package -P ext` - builds the base code and the experiment classes in `src/experiments`
* `mvn package -P tests,mpa` - builds an additional jar for the test classes, note that you also need the `mpa` profile, since the classes are needed for running the tests
* the profiles can also be combined as needed
>>>>>>> 1fe0d2f... new structure for v2.5 submodules
