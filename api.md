# ChangeWindows.org API
We provide some of our data with an API, this includes build information, release information and milestone information. All tables are available as JSON, XML and HTML.

## Builds
**builds** links a release to its milestone.
[JSON](http://changewindows.org/api/cw/builds.json) &middot; [XML](http://changewindows.org/api/cw/builds.xml) &middot; [HTML](http://changewindows.org/api/cw/builds.html)

Field | Description | Status
------------ | ------------- | -------------
build | **Primary key**, contains the build number. | Available
milestone | Contains the id of the milestone this build is part of. | Available

## Releases
**releases** contains all information regarding each individual release. One release is added for each individual ring a build has been released to. So for example, patches for 10240 are released for the Current Branch, Current Branch for Business and Long-Term Support Branch, this means that there are 3 releases with the same data but another ring.
[JSON](http://changewindows.org/api/cw/releases.json) &middot; [XML](http://changewindows.org/api/cw/releases.xml) &middot; [HTML](http://changewindows.org/api/cw/releases.html)

Field | Description | Status
------------ | ------------- | -------------
id | **Primary key**, contains the id of the release. | Available
build | Contains the build number of the release. | Available
string | Contains the string of the release. | Available
platform | Contains an integer from 1 to 6 to represent the platform (in order: desktop, Mobile, Xbox, Server, Holographic, IoT). | Available
ring | Contains an integer from 1 to 6 to represent the branch (in order: Fast, Slow/Preview, Release Preview, Current/Release, Business, LTSB). For desktop and Mobile, 2 and 4 stand for "Slow Ring" and "Current Branch" respectively, since non of the other platforms have such a ring system, these are identified with "Preview" and "Release" respectivly. | Available
date | Contains the date on which the release was released. | Available
announcement | Contains an URL to the announcement of the release or to the KB article on Microsoft.com. | Available

## Milestones
**milestones** contains all information regarding milestones, e.g. Threshold 1, Threshold 2 and Redstone 1.
[JSON](http://changewindows.org/api/cw/milestones.json) &middot; [XML](http://changewindows.org/api/cw/milestones.xml) &middot; [HTML](http://changewindows.org/api/cw/milestones.html)

Field | Description | Status
------------ | ------------- | -------------
id | **Primary key**, identifies a milestone (e.g. 'redstone1'). | Available
name | Official name of the milestone (e.g. 'Anniversary Update'). | Available
version | Version number of the milestone (e.g. '1607'). For milestones that do not have their version announced, it will always use the expected years last 2 digits followed by "99" (e.g. '1799' for Redstone 2). | Available
osname | Contain the name of the OS (e.g. 'Window 10'). | Available
codename | The official codename used within Microsoft (e.g. 'Redstone 1') | Available
description | A description of the milestone. | Available
desktop | Contains the name for the desktop build. | Available
mobile | Contains the name for the Mobile build. | Available
xbox | Contains the name for the Xbox build. | Available
iot | Contains the name for the IoT build. | Available
server | Contains the name for the Server build. | Available
holographic | Contains the name for the Holographic build. | Available
team | Contains the name for the Team build. | Available