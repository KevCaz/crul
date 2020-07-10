crul
====



[![Project Status: Active - The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
[![R-check](https://github.com/ropensci/crul/workflows/R-check/badge.svg)](https://github.com/ropensci/crul/actions/)
[![codecov](https://codecov.io/gh/ropensci/crul/branch/master/graph/badge.svg)](https://codecov.io/gh/ropensci/crul)
[![cran checks](https://cranchecks.info/badges/worst/crul)](https://cranchecks.info/pkgs/crul)
[![rstudio mirror downloads](https://cranlogs.r-pkg.org/badges/crul)](https://github.com/metacran/cranlogs.app)
[![cran version](https://www.r-pkg.org/badges/version/crul)](https://cran.r-project.org/package=crul)

An HTTP client, taking inspiration from Ruby's [faraday](https://rubygems.org/gems/faraday) and Python's `requests`

Package documentation: <https://docs.ropensci.org/crul/>

Some Features:

* `HttpClient` - Main interface to making HTTP requests. Synchronous requests only.
* `HttpResponse` - HTTP response object, used for all responses across the
different clients.
* `Paginator` - Auto-paginate through requests - supports a subset of all possible
pagination scenarios - will fill out more scenarios soon
* `Async` - Asynchronous HTTP requests - a simple interface for many URLS -
whose interface is similar to `HttpClient` - all URLs are treated the same.
* `AsyncVaried` - Asynchronous HTTP requests - accepts any number of `HttpRequest`
objects - with a different interface than `HttpClient`/`Async` due to the nature
of handling requests with different HTTP methods, options, etc.
* set curl options globally: `set_auth()`, `set_headers()`, and more
* Writing to disk and streaming: available with both synchronous requests
as well as async requests
* Hooks on requests and responses are available in the `HttpClient` method only, 
and allow you to trigger functions to run on requests or responses, or both.
See `?hooks` for the details and examples
* Mocking: `crul` integrates with [webmockr](https://github.com/ropensci/webmockr) to mock
HTTP requests. Checkout the [http testing book][book]
* Test caching: `crul` also integrates with [vcr](https://github.com/ropensci/vcr) to cache http requests/responses. Checkout the [http testing book][book]

## Installation

CRAN version


```r
install.packages("crul")
```

Dev version


```r
remotes::install_github("ropensci/crul")
```


```r
library("crul")
```

## Meta

* Please [report any issues or bugs](https://github.com/ropensci/crul/issues).
* License: MIT
* Get citation information for `crul` in R doing `citation(package = 'crul')`
Please note that this package is released with a [Contributor Code of Conduct](https://ropensci.org/code-of-conduct/). By contributing to this project, you agree to abide by its terms.

[![ropensci_footer](https://ropensci.org/public_images/github_footer.png)](https://ropensci.org)

[book]: https://books.ropensci.org/http-testing/
