docs-mysql
==========

Docs for MySQL for [Pivotal Cloud Foundry](https://network.pivotal.io/products/pivotal-cf) (PCF)

## Which branch to use?

**Note**: Provide instructions in your PRs to indicate which branches you want Docs to apply your commits to.

| Branch name | Use for… |
|-------------| -------|
| master      | "edge" branch for 2.x, publishes to https://docs-pcf-staging.cfapps.io/p-mysql/2-n/|
| 2.7         | v2.7.x |
| 2.6         | v2.6.x |
| 2.5         | v2.5.x |
| 2.4         | v2.4.x |
| 2.3         | v2.3.x |
| 2.2         | v2.2.x — PDFed: https://docs.pivotal.io/archives/mysql-docs-2.2.pdf |
| 2.1         | v2.1.x — PDFed: https://docs.pivotal.io/archives/mysql-docs-2.1.pdf |
| 2.0         | v2.0.x — PDFed: https://docs.pivotal.io/archives/mysql-docs-2.0.pdf |
| 1.11        | There are no plans for a v1.11. However, because it publishes to the edge branch, you could use it to stage big changes for the v1.10.x without worrying they'll go to production prematurely. |
| 1.10        | v1.10.x |
| 1.9         | v1.9.x — PDFed: https://docs.pivotal.io/archives/mysql-docs-1.9.pdf |

**Note**: Branches v1.9 through v1.4, v2.0 and v2.1 are no longer published as live documentation. However, documentation for those versions of PDFs is available as PDFs.

## Partials

Cross-product partials for **MySQL for PCF** are single sourced from the [Services Partials](https://github.com/pivotal-cf/docs-partials) repo.

Previously, these partials were sourced from the v018.x branch of the [On Demand Service Broker SDK](https://github.com/pivotal-cf/docs-on-demand-service-broker/tree/v0.18.x) content repo.

## Style Guide

This is a word list for terminology and word usage specific to the MySQL for PCF docs.

| Word | Explanation |
|------|-------------|
| highly available cluster | No need to capitalize. Don't mix with "high availability cluster" or Galera. Galeria happens to be the technology right now, but highly available cluster is the topology. You can abbreviate to HA cluster after spelling out on first use. Don't use "HAC". |
| leader-follower | It seems that we always hyphenate it. But we don't capitalize it. |
| MySQL database cluster node | Only applies to Galera clusters. Spell out like this at first use, then opt for "node" on the rest of the page. |
| node | See above. The old proxy page used: MySQL node, server node, MySQL servers, cluster back-ends, Backend database cluster node, database node VM, proxy instance, proxy. But, only two things are referred to here, nodes and proxies. |
| proxy | Use proxy consistently instead of alternating between "proxy instance" and "proxy". |


## Steps for local development
```
$ git clone git@github.com:pivotal-cf/docs-layout-repo
$ git clone git@github.com:pivotal-cf/docs-mysql
$ cd docs-mysql && git checkout <branch> && cd -
$ git clone git@github.com:pivotal-cf/docs-book-mysql
$ cd docs-book-mysql
$ bundle install
$ bundle exec bookbinder watch
$ open http://127.0.0.1:XXXX/p-mysql/<branch>
```
