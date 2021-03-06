# StatProfilerHTML

| **PackageEvaluator**           | **Build Status**                                                | **Test coverage**                                       |
|:------------------------------:|:---------------------------------------------------------------:|:-------------------------------------------------------:|
|[![][pkg-0.6-img]][pkg-0.6-url] | [![][travis-img]][travis-url] [![][appveyor-img]][appveyor-url] | [![Coverage Status][coveralls-img]][coveralls-url]      |


This module formats the output from Julia's Profile module into an html
rendering of the source function lines and functions, allowing for interactive
exploration of any bottlenecks that may exist in your code.

Have a look [at this example output](http://www.infty.nl/StatProfilerHTML.jl/example-output/), which
is the result of profiling

    using MultivariatePolynomials
    @polyvar x y z
    @profile (x + y + z)^120;


This module contains a fork of the rendering part of Mattia Barbon and Steffen
Müller's excellent
[Devel::StatProfiler](https://github.com/mbarbon/devel-statprofiler), which is
a statistical profiler for Perl. It depends on Text::MicroTemplate, which for
convenience, we ship as part of this bundle.

[travis-img]: https://travis-ci.org/tkluck/StatProfilerHTML.jl.svg?branch=master
[travis-url]: https://travis-ci.org/tkluck/StatProfilerHTML.jl

[appveyor-img]: https://ci.appveyor.com/api/projects/status/mwnbnfp1gjm8ux3d?svg=true
[appveyor-url]: https://ci.appveyor.com/project/tkluck/statprofilerhtml-jl

[pkg-0.6-img]: http://pkg.julialang.org/badges/StatProfilerHTML_0.6.svg
[pkg-0.6-url]: http://pkg.julialang.org/?pkg=StatProfilerHTML

[coveralls-img]: https://coveralls.io/repos/github/tkluck/StatProfilerHTML.jl/badge.svg?branch=master
[coveralls-url]: https://coveralls.io/github/tkluck/StatProfilerHTML.jl?branch=master
