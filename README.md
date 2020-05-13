## specification-v2-test-schemas
#### Test versions of schemas from the Beacon v2 development project

This repository contains test representations of schemas from the Beacon v2 development project. Schemas here are represented as separate files, in concordance with schema representations used by the [GA4GH Schemablocks {S}[B]](https://schemablocks.org/categories/schemas.html) initiative.

Briefly, single schemas extracted from the Beacon v2 code base are deparsed into [JSON](./generated/json/), [examples](./generated/examples/) and [Markdown](./generated/doc/) documentation files as well as being equipped with metadata and processed into web pages utilizing the Jekyll / GitHub Pages system.

The representations here should be considered ephemeral and non-autoritive!

----

### Information for Beacon v2 developers

The complete test setup relies on the existence of clones of 3 project 
directories, in the same parent directory:

* `specification-v2-test-schemas`
  - this repository, which contains some tool scripts and otherwise receives the
  generated files (except the Jekyll input files)
* `specification-v2`
  - the donor repository, containing the (OpenAPI YAML) specification file
* `ga4gh-beacon.github.io`
  - the Beacon project website repository, i.e. a Github Pages source repository

From the parent directory, a complete process to convert & show the schema
information consists of basically 3 commands:

```
python3 specification-v2-test-schemas/sbOpenAPIparser/sbOpenAPIparser.py
perl specification-v2-test-schemas/sbSchemaParser/sbSchemaParser.pl
cd ga4gh-beacon.github.io
bundle exec jekyll serve
```

The use of a local test server requires the proper setup for Jekyll; some help
can be found through the [Progenetix :: Template](https://progenetix.github.io/progenetix-site-template/howto/jekyllinstallation/)
project.