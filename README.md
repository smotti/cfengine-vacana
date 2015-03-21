# Description

A CFEngine framework that come with a comprehensive set of predefined methods
and integrated reporting (central reporting).
It also come with a web frontend to list available hosts, inventories and
promise outcomes.

---

# Why

* NCF is outdated and does to much with service approach
    * Just provide prebuild bundles with proper reporting
    * But provide the bundles that NCF and EFL have
* EFL data driven approach is great but not flexible enough
* Policies written in CFEs declarative language allow for better documentation
* Lack of a good lightweigth and simple to setup dashboard

---

# What

* Include (CFE masterfiles)
    * custom controls (agent, server, ...)
    * custom update.cf (modified version of EFL one)
    * custom cfe_internals
	* Log rotation
	* Remove reports
    * common task bundles (see NCF and EFL)
	* With reporting
    * host info report
    * services autorun
