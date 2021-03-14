## specification-v2-blocks
#### "Blockified" schemas from Beacon v2

This repository contains schemas from the Beacon v2 development project. Schemas here are represented as separate files, in concordance with schema representations used by the [GA4GH Schemablocks {S}[B]](https://schemablocks.org/categories/schemas.html) initiative.

The rendered documentation pages are available trough the **[Beacon project website](https://beacon-project.io/tags/v2.html)**.

The representations here should be considered **ephemeral and non-autoritive!**

----

### Information for Beacon v2 developers

The complete test setup relies on the existence of clones of 3 project 
directories, in the same parent directory:

* `specification-v2-blocks`
  - this repository, which contains some tool scripts and otherwise receives the
  generated files (except the Jekyll input files)
* `specification-v2`
  - the donor repository, containing the (OpenAPI YAML) specification file
* `ga4gh-beacon.github.io`
  - the Beacon project website repository, i.e. a Github Pages source repository

<<<<<<< Updated upstream
From this directory, a complete process to convert & show the schema
information consists of basically 2 commands:

```
python3 ./sbOpenAPIparser/sbOpenAPIparser.py
perl ./sbSchemaParser/sbSchemaParser.pl
```

Briefly, single schemas extracted from the Beacon v2 code base are deparsed into [JSON](./generated/json/), [examples](./generated/examples/) and [Markdown](./generated/doc/) documentation. Also, web pages are generated in the corresponding web project utilizing the Jekyll / GitHub Pages system - this is done by potentially processing projects. Please see / edit the configuration filea at

* [sbOpenAPIparser/config.yaml](./sbOpenAPIparser/config.yaml)
  - e.g. source file definition and header configuration
* [sbSchemaParser/config.yaml](./sbSchemaParser/config.yaml)
  - e.g. processing/target directories

Optional: With a working Jekyll / Github pages environment the pages can now be checked on a locally served version of the site:

```
cd ../ga4gh-beacon.github.io
=======
From *this directory*, a complete process to convert & show the schema
information consists of basically 3 commands:

```
python3 ./tools/sbOpenAPIparser.py -c ./config/sbOpenAPIparser.yaml
perl ./tools/sbSchemaParser.pl -c ./config/sbSchemaParser.yaml
cd ga4gh-beacon.github.io
>>>>>>> Stashed changes
bundle exec jekyll serve
```
... or `bundle exec jekyll build` to just compile the website.

Briefly, single schemas extracted from the Beacon v2 code base are deparsed into [JSON](./generated/json/), [examples](./generated/examples/) and [Markdown](./generated/doc/) documentation. Also, web pages are generated in the corresponding web project utilizing the Jekyll / GitHub Pages system - this is done by potentially processing projects. Please see / edit the configuration filea at

* [sbOpenAPIparser/config.yaml](./sbOpenAPIparser/config.yaml)
  - e.g. source file definition and header configuration
* [sbSchemaParser/config.yaml](./sbSchemaParser/config.yaml)
  - e.g. processing/target directories

Optional: With a working Jekyll / Github pages environment the pages can now be checked on a locally served version of the site:

```
cd ../ga4gh-beacon.github.io
bundle exec jekyll serve
```
... or `bundle exec jekyll build` to just compile the website.

The use of a local test server requires the proper setup for Jekyll; some help
can be found through the [Progenetix :: Template](https://progenetix.github.io/progenetix-site-template/howto/jekyllinstallation/)
project.
