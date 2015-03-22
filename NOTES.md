* Need to take a closer look at the inventory stuff
    * How does it differ from the host info report?
    * How can we laverage it?
    * They mentioned using bundlesmatching/valuesmatching when using it
      with the community edition, but how?
	* Maybe make some tests with it
* Take a look at the lastseen stuff
    * There's also a tool/script from Mark to read them directly from the db
    * And there's also a tool i think to dump the database(s)
* Don't need extra classes bundles, because they are evaluated before methods,
  so they can be specified before all the method calls, and one can use
  classes defined by bundles to conditioninally run other methods
