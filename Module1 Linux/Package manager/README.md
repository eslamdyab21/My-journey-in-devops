
![](https://super.so/icon/light/edit-3.svg)

Package manager
===============

Project

[![](https://super.so/icon/light/folder-plus.svg)Module1: Linux](https://www.notion.so/Module1-Linux-012f8f8155f745f68053f61714910da8)

Area

https://www.notion.so/db4d3f8fd47546eebe52fe130a4b4108



\-Module1: Linux-

Created Time

@June 28, 2022 11:21 PM

Finished At

@June 28, 2022 11:45 PM

Related to Uni Courses (Active Tasks)

APT
---

*   apt package manager is used to install packages/programs in linux.

*   apt install the program with its dependencies

*   it downloads those packages from the internet from hosted repositories, and those repositories can be found in `/etc/apt/sources.list`
    
    [![](Package%20manager%20e47d1f9fae6548a191994609f7f2c5c1/Untitled.png)](Package%20manager%20e47d1f9fae6548a191994609f7f2c5c1/Untitled.png)
    

Snap
----

*   some applications are not in apt, an alternative is `snap`

*   snap snaps all the dependencies in one package and downloads it, this means if tow apps have some shared dependencies it will download them two times one for each app. But apt will only download them once.

*   so if an app is available in both apt and snap, it’s better to download it from apt (less space)

PPA Repository
--------------

*   some applications are not in apt and snap, an alternative is adding a `PPA repository`

*   Personal Package Archive (PPA) are provided by the community, usually used by developers to provide updates more quickly than in the official Ubuntu repositories.

*   because it’s personal (any one can create it) be aware of possible risks before adding a PPA.

*   after adding the PPA (it will be added to the sources.list) and when installing an app the apt toll will now search in the PPA added repo too to fetch the package from that repo.

[![](Package%20manager%20e47d1f9fae6548a191994609f7f2c5c1/Untitled%201.png)](Package%20manager%20e47d1f9fae6548a191994609f7f2c5c1/Untitled%201.png)

Different source based distributions have different package mangers
-------------------------------------------------------------------

*   Debian based: - Ubuntu - Debian - Mint Have APT and APT-GET

*   Red Had based: - RHEL - CentOS - Fedora Have Yum

The concepts of APT and YUM are the same with some differences in the repos, some will have more or newer versions of packages.

And when choosing a distribution for the server the above factors will determine which distro to install.