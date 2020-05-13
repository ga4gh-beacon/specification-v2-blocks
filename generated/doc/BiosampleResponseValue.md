
<div id="schema-header-title">
  <h2>BiosampleResponseValue <span id="schema-header-title-project">beacon <a href="https://github.com/ga4gh-beacon/specification-v2-doc" target="_BLANK">&nearr;</a></span> </h2>
</div>

<table id="schema-header-table">
  <tr>
    <th>{S}[B] Status <a href="https://schemablocks.org/about/sb-status-levels.html">[i]</a></th>
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
<li>Sabela de la Torre Pernas</li>
<li>Jordi Rambla De Argila</li>
<li><a href="https://orcid.org/0000-0002-9903-4248">Michael Baudis</a></li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>Source (2.0)</th>
    <td>
      <ul>
        <li><a href="current/BiosampleResponseValue.json" target="_BLANK">raw source [JSON]</a></li>
        <li><a href="https://github.com/ga4gh-beacon/specification-v2-doc/blob/master/schemas/BiosampleResponseValue.yaml" target="_BLANK">Github</a></li>
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
    <th>error</th>
    <td>./BeaconError</td>
  </tr>
  <tr>
    <th>exists</th>
    <td>boolean</td>
  </tr>
  <tr>
    <th>results</th>
    <td>array of "./BiosampleResponseResults"</td>
  </tr>

</table>


#### error

* type: ./BeaconError




#### exists

* type: boolean

Indicator of whether any biosample was observed in any of the
datasets queried. This should be non-null, unless there was an
error, in which case `error` has to be non-null.



#### results

* type: array of "./BiosampleResponseResults"




