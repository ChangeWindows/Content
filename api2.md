# ChangeWindows 3.5.1702 API
We provide some of our data with an API, this includes build information, release information and milestone information. All tables are available as JSON, XML and HTML.

The API documentation as noted below will take effect on February 2017 and will replace the current ChangeWindows 3.4.1701 API. Note that changes can still be made.

## Builds
**builds** links a release to its milestone.
[JSON](http://changewindows.org/api/cw/builds.json) &middot; [XML](http://changewindows.org/api/cw/builds.xml) &middot; [HTML](http://changewindows.org/api/cw/builds.html)

Field | Description
------------ | -------------
build | **Primary key**, contains the build number
milestone | Contains the id of the milestone this build is part of

## Releases
**releases** contains all information regarding each individual release. Each platform has its own individual release.
[JSON](http://changewindows.org/api/cw/releases.json) &middot; [XML](http://changewindows.org/api/cw/releases.xml) &middot; [HTML](http://changewindows.org/api/cw/releases.html)

Field | Description
------------ | -------------
id | **Primary key**, contains the id of the release
build | Contains the build number of the release
string | Contains the string of the release
platform | Contains an integer from 1 to 7 to represent the platform (in order: PC, Mobile, Xbox, Server, Holographic, IoT, Team)
announcement | Contains an URL to the announcement of the release or to the KB article on Microsoft.com
fast | Contains the date of release for the Fast Ring
slow | Contains the date of release for the Slow Ring or regular Previews
preview | Contains the date of release for the Release Preview Ring
current | Contains the date of release for the Current Branch
business | Contains the date of release for the Current Branch for Business
lts | Contains the date of release for the Long-Term Support Branch
leak | Contains a boolean indicating if the build was leaked or not, also true for vNext listings

## Milestones
**milestones** contains all information regarding milestones, e.g. Threshold 1, Threshold 2 and Redstone 1.
[JSON](http://changewindows.org/api/cw/milestones.json) &middot; [XML](http://changewindows.org/api/cw/milestones.xml) &middot; [HTML](http://changewindows.org/api/cw/milestones.html)

Field | Description
------------ | -------------
id | **Primary key**, identifies a milestone (e.g. 'redstone1')
name | Official name of the milestone (e.g. 'Anniversary Update')
version | Version number of the milestone (e.g. '1607'). For milestones that do not have their version announced, it will always use the expected years last 2 digits followed by "99" (e.g. '1799' for Redstone 2)
osname | Contain the name of the OS (e.g. 'Window 10')
codename | The official codename used within Microsoft (e.g. 'Redstone 1')
description | A description of the milestone

## Statistics
**statistics** contains all information regarding version share between Windows 10 versions.
[JSON](http://changewindows.org/api/cw/statistics.json) &middot; [XML](http://changewindows.org/api/cw/statistics.xml) &middot; [HTML](http://changewindows.org/api/cw/statistics.html)

Field | Description
------------ | -------------
id | **Primary key**, contains the id of the data
date | Date of the month, depicted in an YYMM notation (e.g. '1611' for November 2016)
m[YYMM] | Each version of Windows has its own field in this table, e.g. 'm1507' for the original release. For every new version, a new field with this notation is added