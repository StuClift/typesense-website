---
layout: page
title: Typesense vs Algolia vs ElasticSearch vs Meilisearch
nav_label: support
permalink: /typesense-vs-algolia-vs-elasticsearch-vs-meilisearch/
---

<div class="row no-gutters" xmlns="http://www.w3.org/1999/html">
  <div id="doc-col" class="col-md-12">
    <div class="row">
      <div class="col-md-12">
        <p>
          This following content is based on each search engine's documentation and is meant to provide you with an
          objective side-by-side comparison.
        </p>
      </div>
    </div>
    <div class="row mt-3">
      <div class="col-md-12">
        <h3 class="mb-3">Overview</h3>
        <div class="table-responsive">
          <table class="table table-condensed feature-list">
            <thead class="thead-light">
            <tr>
              <th scope="col"></th>
              <th scope="col">Typesense</th>
              <th scope="col">Algolia</th>
              <th scope="col">ElasticSearch</th>
              <th scope="col">Meilisearch</th>
            </tr>
            </thead>
            <tbody>
            <tr>
              <td class="font-weight-bold">Source Code</td>
              <td>Fully open source</td>
              <td>Proprietary closed source</td>
              <td>Source-available, licensed under SSPL</td>
              <td>Fully open source, with plans for closed-source extensions in the future</td>
            </tr>
            <tr>
              <td class="font-weight-bold">First Commit</td>
              <td>2015</td>
              <td>2012</td>
              <td>2010</td>
              <td>2018</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Built Using</td>
              <td>C++</td>
              <td>C++</td>
              <td>Java</td>
              <td>Rust</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Core Search Algorithm</td>
              <td>Built from the ground-up</td>
              <td>Built from the ground-up</td>
              <td>Built on top of Lucene</td>
              <td>Built from the ground-up</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Best Suited For</td>
              <td>Instant Search-as-you-type Experiences for data sets that can be fit in RAM, up to 768 GB (or current commercially available RAM size).</td>
              <td>Instant Search-as-you-type Experiences for datasets up to 128 GB in size.</td>
              <td>General-purpose search & aggregations over petabyte-scale datasets (eg: log data)</td>
              <td>Instant Search-as-you-type Experiences for up to 10M records, that don't require a highly available
                deployment.
              </td>
            </tr>
            <tr>
              <td class="font-weight-bold">Primary Index Location</td>
              <td>RAM</td>
              <td>RAM</td>
              <td>Disk, with RAM cache</td>
              <td>RAM</td>
            </tr>
            </tbody>
          </table>
        </div>

        <h3 class="mt-5 mb-3">Deployment Options</h3>
        <div class="table-responsive">
          <table class="table table-condensed feature-list">
            <thead class="thead-light">
            <tr>
              <th scope="col"></th>
              <th scope="col">Typesense</th>
              <th scope="col">Algolia</th>
              <th scope="col">ElasticSearch</th>
              <th scope="col">Meilisearch</th>
            </tr>
            </thead>
            <tbody>
            <tr>
              <td class="font-weight-bold">Self Hosted Option</td>
              <td>✅️</td>
              <td>❌</td>
              <td>✅️</td>
              <td>✅️</td>
            </tr>
            <tr>
              <td class="font-weight-bold">SaaS Option</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>❌</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Fault Tolerance</td>
              <td>RAFT-based clustering</td>
              <td>RAFT-based clustering</td>
              <td>Active-passive replication</td>
              <td>❌</td>
            </tr>
            <tr>
              <td class="font-weight-bold">CDN-like Geo-Distributed clusters</td>
              <td>Supported in self-hosted and SaaS options, called Search Delivery Network</td>
              <td>Supported in SaaS option, called Distributed Search Network</td>
              <td>Supported in self-hosted, Not available as part of hosted offering</td>
              <td>❌</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Dependencies</td>
              <td>Self-contained binary. <br>Built-in high performance HTTP server, that can be exposed to the frontend
                directly.
              </td>
              <td>N/A, since it's SaaS only</td>
              <td>Requires JVM, and an application backend. <br>Cannot be directly exposed to frontend - requires use of
                nginx, apache or the like as a reverse proxy in front
              </td>
              <td>Requires use of nginx, apache or the like as a reverse proxy in front, before exposing to frontend</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Index Backward Compatibility</td>
              <td>✅<br> Fully backward compatible</td>
              <td>✅<br> Fully backward compatible</td>
              <td>✅<br> Fully backward compatible</td>
              <td>❌<br> Not backward compatible across versions. Version upgrades require re-indexing.</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Upgrade Path</td>
              <td>Replace binary, restart process</td>
              <td>Managed SaaS service, doesn't require upgrades</td>
              <td>Replace binary, restart process</td>
              <td>Replace binary, re-index all documents</td>
            </tr>
            </tbody>
          </table>
        </div>

        <h3 class="mt-5 mb-3">Features</h3>
        <div class="table-responsive">
          <table class="table table-condensed feature-list">
            <thead class="thead-light">
            <tr>
              <th scope="col"></th>
              <th scope="col">Typesense</th>
              <th scope="col">Algolia</th>
              <th scope="col">ElasticSearch</th>
              <th scope="col">Meilisearch</th>
            </tr>
            </thead>
            <tbody>
            <tr>
              <td class="font-weight-bold">REST API</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>✅️</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Typo Tolerance</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>✅️<br>But slow and <a
                      href="https://www.algolia.com/blog/engineering/algolia-v-elasticsearch-relevance/" target="_blank">affects
                relevance</a></td>
              <td>✅️</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Query Field Weights / Boosting</td>
              <td>✅️</td>
              <td>❌</td>
              <td>✅️</td>
              <td>❌</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Scoped API Keys / Multi-tenancy</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>❌</td>
              <td>❌</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Federated Search</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>❌</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Grouping / Distinct</td>
              <td>✅️</td>
              <td>✅<br> Upto one distinct field</td>
              <td>✅️</td>
              <td>✅<br> Upto one distinct field</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Dynamic Sorting</td>
              <td>✅<br>Sort fields can be defined at query time using a single index</td>
              <td>❌<br>Duplicate indices need to be created for each sort order</td>
              <td>✅<br>Sort fields can be defined at query time using a single index</td>
              <td>❌<br>Duplicate indices need to be created for each sort order</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Faceting & Filtering</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>✅<br> Only string-type facets</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Facet Value Searches</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>❌</td>
              <td>❌</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Result Pinning / Merchandising</td>
              <td>✅️</td>
              <td>✅<br> Upto 300 results</td>
              <td>✅️</td>
              <td>❌</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Synonyms</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>✅️</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Language support</td>
              <td>All languages, expect logographic ones</td>
              <td>All languages</td>
              <td>All languages</td>
              <td>Latin-based languages, English, and kanji languages</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Stop words</td>
              <td>❌</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>✅️</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Geo Search</td>
              <td>❌</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>❌</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Automatic Record ID generation</td>
              <td>✅</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>❌<br>IDs needs to be pre-generated</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Sort by String field</td>
              <td>❌</td>
              <td>✅<br>But <a
                      href="https://www.algolia.com/doc/guides/managing-results/refine-results/sorting/how-to/sort-an-index-alphabetically/"
                      target="_blank">not recommended</a></td>
              <td>✅️</td>
              <td>❌</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Search Analytics</td>
              <td>Client-side, through InstantSearch.js</td>
              <td>Client-side and Server-side</td>
              <td>❌</td>
              <td>Client-side, through InstantSearch.js</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Record Validations</td>
              <td>✅️</td>
              <td>❌</td>
              <td>✅<br> with coerced mapping</td>
              <td>❌</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Custom Ranking Rules</td>
              <td>✅<br> Upto 3 fields</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>✅️</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Negative Keyword Search <br>(<code>-query</code>)</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>❌</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Exact Keyword Search <br>(<code>"query"</code>)</td>
              <td>❌</td>
              <td>✅️</td>
              <td>✅️</td>
              <td>❌</td>
            </tr>
            <tr>
              <td class="font-weight-bold">User-level Search Personalization</td>
              <td>❌</td>
              <td>✅<br> Premium Tier</td>
              <td>❌</td>
              <td>❌</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Collection Aliases</td>
              <td>✅️</td>
              <td>❌</td>
              <td>✅️</td>
              <td>❌</td>
            </tr>
            <tr>
              <td class="font-weight-bold">A/B Testing Results</td>
              <td>❌</td>
              <td>✅<br> Premium Tier</td>
              <td>❌</td>
              <td>❌</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Query Suggestions</td>
              <td>❌</td>
              <td>✅️</td>
              <td>❌</td>
              <td>❌</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Visual Dashboard</td>
              <td>❌</td>
              <td>✅️</td>
              <td>✅️<br>3rd party plugins</td>
              <td>✅️<br>Search only</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Site Crawler</td>
              <td>❌</td>
              <td>✅<br>Premium Tier</td>
              <td>❌</td>
              <td>❌</td>
            </tr>
            <tr>
              <td class="font-weight-bold">UI Component Library</td>
              <td>✅<br>Supports InstantSearch.js</td>
              <td>✅<br>InstantSearch.js</td>
              <td>✅<br>Search UI, requires hosted search</td>
              <td>✅<br>Supports InstantSearch.js</td>
            </tr>
            </tbody>
          </table>
        </div>

        <h3 class="mt-5 mb-3">Limits</h3>
        <div class="table-responsive">
          <table class="table table-condensed feature-list">
            <thead class="thead-light">
            <tr>
              <th scope="col"></th>
              <th scope="col">Typesense</th>
              <th scope="col">Algolia</th>
              <th scope="col">ElasticSearch</th>
              <th scope="col">Meilisearch</th>
            </tr>
            </thead>
            <tbody>
            <tr>
              <td class="font-weight-bold">Index Count Limit</td>
              <td>No limitation</td>
              <td>No limitation</td>
              <td>No limitation</td>
              <td>200</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Index Size Limit</td>
              <td>No technical limits, constrained by available RAM</td>
              <td>128 GB</td>
              <td>No limitation</td>
              <td>100GB default, can be modified</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Maximum Words per field</td>
              <td>No limitation</td>
              <td>No limitation</td>
              <td>No limitation</td>
              <td>1000</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Record Size Limit</td>
              <td>No limitation</td>
              <td>10KB</td>
              <td>No limitation</td>
              <td>Not published</td>
            </tr>
            </tbody>
          </table>
        </div>

        <h3 class="mt-5 mb-3">Support</h3>
        <div class="table-responsive">
          <table class="table table-condensed feature-list">
            <thead class="thead-light">
            <tr>
              <th scope="col"></th>
              <th scope="col">Typesense</th>
              <th scope="col">Algolia</th>
              <th scope="col">ElasticSearch</th>
              <th scope="col">Meilisearch</th>
            </tr>
            </thead>
            <tbody>
            <tr>
              <td class="font-weight-bold">Channels</td>
              <td>Github issues<br> Email<br> Community<br> Slack<br> Paid Prioritized Support</td>
              <td>Github issues<br> Email<br> Community<br> Paid Prioritized Support</td>
              <td>Github issues<br> Email<br> Community<br> Paid Prioritized Support</td>
              <td>Github issues<br> Email<br> Community</td>
            </tr>
            <tr>
              <td class="font-weight-bold">Export Onboarding & Training</td>
              <td>✅</td>
              <td>✅</td>
              <td>✅</td>
              <td>❌</td>
            </tr>
            </tbody>
          </table>
        </div>

        <p class="mt-5">
          We've strived to provide accurate information above, but if you notice any issues, please open an issue <a
                href="https://github.com/typesense/typesense-website/issues" target="_blank">here</a>.
        </p>
      </div>
    </div>
  </div>
</div>
