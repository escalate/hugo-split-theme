# How to contribute to Split

## Pull requests

Please follow the [Conventional Commits 1.0.0 specification](https://www.conventionalcommits.org/en/v1.0.0/) to format your commit message. One commit per change is preferred.

## Testing

There are two test sites under [`tests/exampleSiteWithImage`](./tests/exampleSiteWithImage) and [`tests/exampleSiteWithVideo`](tests/exampleSiteWithVideo). Please adjust those accordingly
to the changes you have made resp. check if your change didn't introduce any [regressions](https://en.wikipedia.org/wiki/Regression_testing).

You can run these using the [`Makefile`](./Makefile) found at the root of this repository:

`$ make hugo-server-example-site-with-image`\
`$ make hugo-server-example-site-with-video`
