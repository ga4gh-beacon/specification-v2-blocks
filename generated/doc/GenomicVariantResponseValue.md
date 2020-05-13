
<div id="schema-header-title">
  <h2>GenomicVariantResponseValue <span id="schema-header-title-project">[beacon-v2] <a href="https://github.com/ga4gh-beacon/specification-v2-test-schemas" target="_BLANK">&nearr;</a></span> </h2>
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
<li>Sabela de la Torre Pernas (__contributor_ORCID__)</li>
<li>Sabela de la Torre Pernas (__contributor_ORCID__)</li>
<li>Michael Baudis (ORCID:0000-0002-9903-4248)</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Source (2.0)</th>
    <td>
      <ul>
        <li><a href="current/GenomicVariantResponseValue.json" target="_BLANK">raw source [JSON]</a></li>
        <li><a href="https://github.com/ga4gh-beacon/specification-v2-test-schemas/blob/master/schemas/GenomicVariantResponseValue.yaml" target="_BLANK">Github</a></li>
      </ul>
    </td>
  </tr>
</table>

<div id="schema-attributes-title">
  <h3>Attributes</h3>
</div>

  
__Type:__ object  
__Description:__ Description pending

### Properties

<table id="schema-properties-table">
  <tr>
    <th>Property</th>
    <th>Type</th>
  </tr>
  <tr>
    <th>beaconHandover</th>
    <td>./Handover</td>
  </tr>
  <tr>
    <th>error</th>
    <td>./BeaconError</td>
  </tr>
  <tr>
    <th>exists</th>
    <td>boolean</td>
  </tr>
  <tr>
    <th>info</th>
    <td>object</td>
  </tr>
  <tr>
    <th>results</th>
    <td>array of "./VariantReponseResults"</td>
  </tr>
  <tr>
    <th>resultsHandover</th>
    <td>./Handover</td>
  </tr>

</table>


#### beaconHandover

* type: ./Handover




#### error

* type: ./BeaconError




#### exists

* type: boolean

Indicator of whether any variant was observed in any of the
datasets queried. This should be non-null, unless there was an
error, in which case `error` has to be non-null.



#### info

* type: object




#### results

* type: array of "./VariantReponseResults"




#### resultsHandover

* type: ./Handover




