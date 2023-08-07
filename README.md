# CLiSN <:books:>:sparkles:
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

A collection of [RDFLib](https://rdflib.readthedocs.io/en/stable/) namespaces for the [Computational Literary Studies Infrastructure](https://clsinfra.io/) project.

## Requirements
* Python >=3.11

## Installation

## Usage

### Namespaces
CLiSN provides `rdflib.Namespaces` for the CLSInfra project.

```python
# todo: find a good example.
```

Note that `from clisn import *` imports `rdflib.Namespace` instances only. Please always use explicit imports.


### NamespaceManager

`clisn` features a custom [NamespaceManager](https://rdflib.readthedocs.io/en/stable/apidocs/rdflib.namespace.html#rdflib.namespace.NamespaceManager) for CLSInfra namespaces.
This e.g. allows to easily generate a namespaced `rdflib.Graph` like so:

```python
from rdflib import Graph, URIRef, Literal
from clisn import CLSInfraNamespaceManager, crm

graph = Graph()
CLSInfraNamespaceManager(graph)

graph.add(
    (
        URIRef("subject"),
        crm["p90_has_value"],
        Literal("some value")
    )
)
```
