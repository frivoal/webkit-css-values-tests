This repo contains copies of the tests from https://trac.webkit.org/browser/webkit/trunk/LayoutTests/css3/calc as of revision 239665,
with a series of fixes to make them:
* correct according to the latest spec
* acceptable for submission to [WPT](https://github.com/web-platform-tests/wpt)

This is meant as a working space for [TalbotG](https://github.com/TalbotG/) and [frivoal](https://github.com/frivoal)
so that we can work on the tests themselves,
before worying about the right way to submit them to Webkit and/or WPT.

The following test should not be ported to WPT, since they test features that are neither standard features nor documented in https://compat.spec.whatwg.org/:
* simple-calcs-prefixed.html
* zoom-with-em.html
* box-reflect.html
* webkit-gradient-calc.html
* reflection-computed-style.html


The following tests could be ported to WPT, as they test standard features, but as they are crash tests rather than conformance tests, it is not certain whether that's useful:
* transition-crash.html
* transition-crash2.html
* transition-crash3.html
* transition-crash4.html
* lexer-regression-57581.html
* lexer-regression-57581-2.html
* lexer-regression-57581-3.html
* regression-62276.html
* cubic-bezier-with-multiple-calcs-crash.html.html

The following tests check behavior that isn't actually defined, and it looks like it might not end up being defined the same way as the tests expect (see https://drafts.csswg.org/css-values-3/#calc-serialize or https://drafts.csswg.org/css-values-4/#calc-serialize):
* getComputedStyle-margin-percentage.html
* cssom.html
* simple-calcs.html
* simplification.html

Everything else should be added to WPT.

----

Todo: finish reviewing and converting the following tests:
* transitions-dependent.html
* transitions.html
