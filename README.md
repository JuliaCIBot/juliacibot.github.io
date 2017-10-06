## JuliaCIBot

JuliaCIBot runs tests on pull requests to [METADATA.jl](https://github.com/JuliaLang/METADATA.jl). Tests are run for the tagged version of the package and its previous version if any. The tests are run for the current release version of julia and the previous release. Packages that depend on the tagged package are also tested. Although, we can only test a limited number of such "reverse dependencies" due to the time it takes to test all packages.

A pull request is deemed to pass CI if tests pass for the tagged version of the package and there are no test failures introduced in the reverse dependencies due to this tag. The results of the test are shown in a table with 2 columns to compare the current version and the proposed tag. The *pass* and *fail* markers link to the logs of the test. If the test has failed for a pull request then the rows tinted red indicate the tests that need to pass. For example:

![CI example](https://github.com/JuliaCIBot/juliacibot.github.io/raw/master/images/ci_example.png "CI example")

We hope to develop the CI process to a stage where we can automate merging of pull requests. To help us, please report issues to [ci@juliacomputing.com](mailto:ci@juliacomputing.com)
