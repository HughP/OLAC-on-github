# OLAC-on-github
A Repository to discuss how to advertise github projects on olac.
Included in this repo are initial drafts of YAML and TOML templates.


## Background
[OLAC](http://www.language-archives.org) is a service run by a community of language archives. The service makes metdata (record listings) available for search engines, highlighting among other things the languages to which a resource applies.

[Github](https://github.com) has entered various social spaces including the linguistic data domain and the software for minority languages domain. Both of these domains are under-represented in OLAC indexes.

There are several reasons for this under representation.

1. OLAC is primarily an XML technology. Many software developers today prefer to use JSON to describe data.
2. OLAC has generally primarily gained traction among the digitally savvy archivists who have been engaged with the open archives and endangered languages movements. Leaving developers in other communities of the loop.
3. OLAC services are seen by archives as secondary to individual branding efforts vying for the attention of linguists and community members.

## Solution
How can we rectify the problem of finding language tools and resources which are hosted on github?

1. We can create a JSON template that developers  and data providers can clone, modify and add to the root of a repo, or a repo in a github organization. This template would include some basic [DOAP](https://github.com/ewilderj/doap) and OLAC fields.
2. We can write a service which scans github for these files, finds them and then harvests the file, and other relevant data via the github API, consolidates these files into a single XML file (of course in the OLAC compliant format) and then pushes that XML file to a repo which the OLAC service monitors.

The exact mechanics of how `#2` works out, needs to be negotiated.
* It seems that this sort of thing could be accomplished with Travis-CI. (But if that doesn't work out I have a rasberry pi that we could use). 
* It also seems possible that YAML or TOML might be able to be used, but the internationalization of strings would need to be tested.
* OLAC calls for an archive description, and assumes an institutional framework. Github in this case is not the data provider or publisher. In some cases a github "organization" may be the provider. In other cases it might be an individual with only one repository. There should be some experimentation to determine the simplest but most efficient path is for human interaction and contribution. Some individuals
* github is not the only provider there is also gitlab, and a blossoming industry of data and archive like services.
* The github scanning service should make a complied index and a current index. One will focus on what is currently avaible, while the other would keep a record of what has been listed in the past. Sometimes records can be removed. While OLAC is most interested in the "current index", a past index is very useful for a variety of reasons.

Included in this repo are initial drafts of YAML and TOML templates.
