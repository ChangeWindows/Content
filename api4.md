# ChangeWindows 4.0.1704 API
We provide some of our data with an API, this includes build information, release information and milestone information. All tables are available as JSON, XML and HTML. This API is compatible with 4.0.1704.

## Builds
**builds** links a release to its milestone.
[JSON](http://changewindows.org/api/cw/builds.json) &middot; [XML](http://changewindows.org/api/cw/builds.xml) &middot; [HTML](http://changewindows.org/api/cw/builds.html)

Field | Description
------------ | -------------
build | **Primary key**, contains the build number
milestone | Contains the id of the milestone this build is part of

## Releases
**releases** contains all information regarding each individual release. One release is added for each individual ring a build has been released to. So for example, patches for 10240 are released for the Current Branch, Current Branch for Business and Long-Term Support Branch, this means that there are 3 releases with the same data but another ring.
[JSON](http://changewindows.org/api/cw/releases.json) &middot; [XML](http://changewindows.org/api/cw/releases.xml) &middot; [HTML](http://changewindows.org/api/cw/releases.html)

Field | Description
------------ | -------------
id | **Primary key**, contains the id of the release
build | Contains the build number of the release
string | Contains the string of the release
platform | Contains an integer from 1 to 7 to represent the platform (see below)
ring | Contains an integer from 1 to 8 to represent the branch (see below)
date | Contains the date on which the release was released

### platform int
int | Platform
------------ | -------------
1 | PC
2 | Mobile
3 | Xbox
4 | Server
5 | Holographic
6 | IoT
7 | Team

### ring int
int | Ring | Platform
------------ | ------------- | -------------
1 | Leak | 
2 | Fast Ring | PC, Mobile, Xbox
3 | Slow Ring | PC, Mobile, Xbox
4 | Preview | Xbox, Server, Holographic, IoT
5 | Release Preview Ring | PC, Mobile, Xbox
6 | Current Branch | PC, Mobile, Xbox, Server, Holographic, IoT, Team
7 | Current Branch for Business | PC, Mobile, Server, Holographic, IoT, Team
8 | Long-Term Support Branch | PC, Server, Holographic, IoT, Team

## Milestones
**milestones** contains all information regarding milestones, e.g. Threshold 1, Threshold 2 and Redstone 1.
[JSON](http://changewindows.org/api/cw/milestones.json) &middot; [XML](http://changewindows.org/api/cw/milestones.xml) &middot; [HTML](http://changewindows.org/api/cw/milestones.html)

Field | Description
------------ | -------------
id | **Primary key**, identifies a milestone (e.g. 'redstone1')
name | Official name of the milestone (e.g. 'Anniversary Update')
version | Version number of the milestone (e.g. '1607'). For milestones that do not have their version announced, it will always use the expected years last 2 digits followed by "99" (e.g. '1799' for Redstone 3)
osname | Contain the name of the OS (e.g. 'Window 10')
codename | The official codename used within Microsoft (e.g. 'Redstone 1')
description | A description of the milestone

## Months
**months** contains a list of months for which ChangeWindows provides statistics.
[JSON](http://changewindows.org/api/cw/months.json) &middot; [XML](http://changewindows.org/api/cw/months.xml) &middot; [HTML](http://changewindows.org/api/cw/months.html)

Field | Description
------------ | -------------
id | **Primary key**, contains the id of the data
date | Contains the date of the months first day

## Stats
**stats** contains individual statistics for each milestone for each month.
[JSON](http://changewindows.org/api/cw/months.json) &middot; [XML](http://changewindows.org/api/cw/months.xml) &middot; [HTML](http://changewindows.org/api/cw/months.html)

Field | Description
------------ | -------------
id | **Primary key**, contains the id of the data
month | Contains the id of the month (see Months-table)
milestone | Contains the id of the milestone to which the data applies (see Milestone-table)
share | Contains the marketshare of the month for its milestone