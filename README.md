potato
======

checking scope resolution in R

basically I wanted to make sure that if I called a package's function
without loading the package, and it called a function within it's own
package, even though the package had not been added to the search path,
the standard scope resolution stuff would still work.

guess what? it does. +1 for Hadley!

example
=======

  $ R

  R version 3.1.1 (2014-07-10) -- "Sock it to Me"
  Copyright (C) 2014 The R Foundation for Statistical Computing
  Platform: x86_64-apple-darwin13.1.0 (64-bit)

  R is free software and comes with ABSOLUTELY NO WARRANTY.
  You are welcome to redistribute it under certain conditions.
  Type 'license()' or 'licence()' for distribution details.

    Natural language support but running in an English locale

  R is a collaborative project with many contributors.
  Type 'contributors()' for more information and
  'citation()' on how to cite R or R packages in publications.

  Type 'demo()' for some demos, 'help()' for on-line help, or
  'help.start()' for an HTML browser interface to help.
  Type 'q()' to quit R.

  > potato::function_a()
  [1] "You called function_a, now I'm going to call function_b"
  [1] "You called function B!"
