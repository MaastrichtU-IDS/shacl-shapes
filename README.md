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

### Generate SHACL Shapes from OWL ontologies

You can use [Astrea](https://astrea.linkeddata.es) to convert OWL ontologies files to SHACL shapes files: https://astrea.linkeddata.es

Example querying it automatically (for the [BioLink model ontology](https://raw.githubusercontent.com/biolink/biolink-model/master/biolink-model.owl.ttl)):

```bash
curl -X POST --header 'Content-Type: application/json' --header 'Accept: text/rdf+turtle' -d '{"ontologies": ["https://raw.githubusercontent.com/biolink/biolink-model/master/biolink-model.owl.ttl"]}' https://astrea.linkeddata.es/api/shacl/url
```

### Generate SHACL Shapes from RDF file

[Shaclgen](https://github.com/uwlib-cams/shaclgen) takes either a instance graph(s) or schema(s) as input and generates a basic shape file based on the classes and properties present: https://github.com/uwlib-cams/shaclgen

### Generate web form from Shapes

[Schímatos](https://schimatos.github.io): a SHACL-based Web-Form Generator for Knowledge Graph Editing (RS). 

Schímatos is a form-based Web application with which users can create and edit data against SHACL constraints. If you are interested in an overview of how the tool works you can check out this video https://youtu.be/PvnJGnB7hOU (we have an abridged version as part of our talk on Wednesday).You can also try the tool for yourself at [https://schimatos.github.io](https://schimatos.github.io/) and visit our GitHub at https://github.com/schimatos/schimatos.org




