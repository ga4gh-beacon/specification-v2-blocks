
<div id="schema-header-title">
  <h2>GenomicVariantFields <span id="schema-header-title-project">[beacon-v2] <a href="https://github.com/ga4gh-beacon/specification-v2-test-schemas" target="_BLANK">&nearr;</a></span> </h2>
</div>

<table id="schema-header-table">
  <tr>
    <th>{S}[B] Status Level <a href="https://schemablocks.org/about/sb-status-levels.html">[i]</a></th>
    <td><div id="schema-header-status">playground</div></td>
  </tr>

  <tr>
    <th>Provenance</th>
    <td>
      <ul>
<li><a href="https://github.com/ga4gh-beacon/specification-v2">Beacon v2 draft schema</a></li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Used by</th>
    <td>
      <ul>
<li><a href="https://github.com/ga4gh-beacon/specification-v2">Beacon, for Beacon v2 testing</a></li>
      </ul>
    </td>
  </tr>

<!--more-->

  <tr>
    <th>Contributors</th>
    <td>
      <ul>
<li><a href="https://beacon-project.io/categories/people.html">ELIXIR Beacon team</a></li>
<li><a href="https://beacon-project.io/people/Sabela-de-la-Torre/">Sabela de la Torre Pernas</a></li>
<li><a href="https://beacon-project.io/people/Jordi-Rambla/">Jordi Rambla De Argila</a></li>
<li><a href="https://orcid.org/0000-0002-9903-4248">Michael Baudis</a></li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Source (2.0)</th>
    <td>
      <ul>
        <li><a href="current/GenomicVariantFields.json" target="_BLANK">raw source [JSON]</a></li>
        <li><a href="https://github.com/ga4gh-beacon/specification-v2-test-schemas/blob/master/schemas/GenomicVariantFields.yaml" target="_BLANK">Github</a></li>
      </ul>
    </td>
  </tr>
</table>

<div id="schema-attributes-title">
  <h3>Attributes</h3>
</div>

  
__Type:__ object  
__Description:__ All the required fields to query any kind of variant (e.g. SNP, DUP, 
etc.).

### Properties

<table id="schema-properties-table">
  <tr>
    <th>Property</th>
    <th>Type</th>
  </tr>
  <tr>
    <th>alternateBases</th>
    <td>string</td>
  </tr>
  <tr>
    <th>assemblyId</th>
    <td>./Assembly</td>
  </tr>
  <tr>
    <th>end</th>
    <td>array of "integer"</td>
  </tr>
  <tr>
    <th>mateName</th>
    <td>./Chromosome</td>
  </tr>
  <tr>
    <th>referenceBases</th>
    <td>string</td>
  </tr>
  <tr>
    <th>referenceName</th>
    <td>./Chromosome</td>
  </tr>
  <tr>
    <th>start</th>
    <td>array of "integer"</td>
  </tr>
  <tr>
    <th>variantType</th>
    <td>string</td>
  </tr>

</table>


#### alternateBases

* type: string

The bases that appear instead of the reference bases. Accepted 
values: [ACGTN]*. N is a wildcard, that denotes the position of any 
base, and can be used as a standalone base of any type or within a 
partially known sequence. For example a sequence where the first and 
last bases are known, but the middle portion can exhibit countless 
variations of [ACGT], or the bases are unknown: ANNT the Ns can take 
take any form of [ACGT], which makes both ACCT and ATGT (or any 
other combination) viable sequences.
Symbolic ALT alleles (DEL, INS, DUP, INV, CNV, DUP:TANDEM, DEL:ME,
INS:ME) will be represented in `variantType`.
Optional: either `alternateBases` or `variantType` is required.



#### assemblyId

* type: ./Assembly




#### end

* type: array of "integer"

Precise or fuzzy end coordinate(s) (0-based, exclusive). See start. 
For fuzzy matches, provide 2 values in the array (e.g. [111,222]).



#### mateName

* type: ./Chromosome




#### referenceBases

* type: string

Reference bases for this variant (starting from `start`). 
Accepted values: [ACGTN]*. N is a wildcard, that denotes the 
position of any base, and can be used as a standalone base of any 
type or within a partially known sequence. For example a sequence 
where the first and last bases are known, but the middle portion can 
exhibit countless variations of [ACGT], or the bases are unknown: 
ANNT the Ns can take take any form of [ACGT], which makes both ACCT 
and ATGT (or any other combination) viable sequences.



#### referenceName

* type: ./Chromosome




#### start

* type: array of "integer"

Precise or fuzzy start coordinate position(s), allele locus 
(0-based, inclusive).
* start only:
  - for single positions, e.g. the start of a specified sequence 
  alteration where the size is given through the specified 
  `alternateBases`
  - typical use are queries for SNV and small InDels
  - THIS IS NOT TRUE FOR RANGE QUERIES!!!! -> the use of "start" 
  without an "end" parameter requires the use of "referenceBases"
* `start` and `end`:
  - special use case for exactly determined structural changes
* use 2 values for querying imprecise positions (e.g. identifying 
all structural variants starting anywhere between `start[0]` <-> 
`start[1]`, and ending anywhere between `end[0]` <-> `end[1]`)
* IS THIS NECESSARY???? -> single or double sided precise matches 
can be achieved by setting `start[0]` = `start[1]` XOR `end[0]` = 
`end[1]`



#### variantType

* type: string

The `variantType` is used to denote e.g. structural variants.
Examples:
* DUP: duplication of sequence following `start`; not necessarily in
situ
* DEL: deletion of sequence following `start`
* BND: breakend, i.e. termination of the allele at position
      `start` or in the `startMin` => `startMax` interval, or fusion
      of the sequence to distant partner
Optional: either `alternateBases` or `variantType` is required.



