# Databricks monorepo example

## Purpose of this repo

A template for a default setup for Databricks files for the projects within an organisation.

It assumes a data mesh-like hierarchy of organization, domain, project, data product and table.

The path expressing the hierarchy could be:

```bash
./orgs/acme/domains/sales/projects/customer_analysis/flows/prep/customer_classification/classifications.py
```
It assumes that classifications.py produces the table `classifications` of the data product `customer_classification`.

## Unity Catalog structure proposal for data products

![docs/images/unity_catalog_structure.png](Unity Catalog Structure proposal).

Note the similarity of the hierarchy in git and unity catalog.

## Test examples

Examples of pyspark tests can be found here:

[./orgs/acme/domains/example/projects/nyctaxi/tests](./orgs/acme/domains/example/projects/nyctaxi/tests)

## libs/repotools

Utility function to add projects folder root as path to the notebook, to enable importing of project specific libs.

## Documentation

Documentation can be added under the `docs` folder.
