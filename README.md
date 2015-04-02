# Description

A lightweight set of CFEngine masterfiles with the vacana library, which
provides logging and a comprehensive set of predefined bundles for the most
common administrativ tasks.

Also note that this library is focused on the latest CFEngine Community
version (currently 3.6.5).

This library can be used with the vacana dashboard.

---

# Why

* NCF is outdated and does to much with service approach
    * Just provide prebuild bundles with proper reporting
    * But provide the bundles that NCF and EFL have
* EFL data driven approach is great but not flexible enough
* Policies written in CFEs declarative language allow for better documentation
* Lack of a good lightweight and simple to setup dashboard (see vacana
  dashboard for a solution)

---

# Try it

You might try it via vagrant. For that you'll need ansible (I'll probably
change that also to the cfengine provisioner), because that's how the
vagrant VM's a provisioned at the moment.
On Debian-based distros:

    :::bash
    apt-get --no-install-recommends --install ansible
    vagrant up hub node

---

# TODO

* Quickstart guide
* Tutorials
* Reference
* More bundles
