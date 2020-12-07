# Repository for SHACL Shapes

A repository for SHACL Shapes at the Institute of Data Science at Maastricht University.

The shapes are automatically retrieved and exposed by the shapes-of-you registry: https://maastrichtu-ids.github.io/shapes-of-you

## Add a new shape

Contributions are welcome! See the [guidelines to contribute 👨‍💻](/CONTRIBUTING.md).

Clone the repository:

```bash
git clone https://github.com/MaastrichtU-IDS/shacl-shapes
cd shacl-shapes
```

Add your shape file, commit, push and send a pull request.

## SHACL shapes resources

### Generate SHACL Shapes from RDF and validate

[SHACL Play](https://shacl-play.sparna.fr/play/) is a platform exposing a few practical tools to build SHACL shapes

* [Generate SHACL shapes from RDF](https://shacl-play.sparna.fr/play/convert) choosing a ruleset
  * OWL to SHACL: open world
  * OWL to SHACL: semi closed
  * OWL to SHACL: closed

* Generate a UML diagram from SHACL shape
* Validate your SHACL shapes
* Add your shapes or rules to their catalogs

### Generate SHACL Shapes from OWL ontologies

You can use [Astrea](https://astrea.linkeddata.es) to convert OWL ontologies files to SHACL shapes files: https://astrea.linkeddata.es

Example querying it automatically (for the [BioLink model ontology](https://raw.githubusercontent.com/biolink/biolink-model/master/biolink-model.owl.ttl)):

```bash
curl -X POST --header 'Content-Type: application/json' --header 'Accept: text/rdf+turtle' -d '{"ontologies": ["https://raw.githubusercontent.com/biolink/biolink-model/master/biolink-model.owl.ttl"]}' https://astrea.linkeddata.es/api/shacl/url
```

### Generate SHACL Shapes from RDF file (smaller project)

[Shaclgen](https://github.com/uwlib-cams/shaclgen) takes either a instance graph(s) or schema(s) as input and generates a basic shape file based on the classes and properties present: https://github.com/uwlib-cams/shaclgen

### Generate web form from Shapes

[Schímatos](https://schimatos.github.io): a SHACL-based Web-Form Generator for Knowledge Graph Editing (RS). 

Schímatos is a form-based Web application with which users can create and edit data against SHACL constraints. If you are interested in an overview of how the tool works you can check out this video https://youtu.be/PvnJGnB7hOU (we have an abridged version as part of our talk on Wednesday).You can also try the tool for yourself at [https://schimatos.github.io](https://schimatos.github.io/) and visit our GitHub at https://github.com/schimatos/schimatos.org

### Make modular shapes
[LODE](https://github.com/dbpedia/archivo/blob/master/shacl-library/LODE.ttl) shows how to make your shapes more modular.


### Validate RDF with SHACL Shapes

To validate RDF against SHACL Shapes and get a human-readable of the issues: https://rdfshape.weso.es/shaclValidate 
