# ChangeWindows.org API
We provide some of our data with an API, this includes build information, ring information and milestone information. All tables are available as JSON, XML and HTML.

## Builds
**builds** contains all information about every single build. This includes build strings, minilogs, release dates and announcement urls. Most of the info in this table will no longer be available for ChangeWindows 3.0 as we move to replace most of this with the **releases**-table.
[JSON](http://changewindows.org/api/cw/builds.json) &middot; [XML](http://changewindows.org/api/cw/builds.xml) &middot; [HTML](http://changewindows.org/api/cw/builds.html)

Field | Description | Status
------------ | ------------- | -------------
build | **Primary key**, contains the build number. | Available
milestone | Contains the id of the milestone this build is part of. | Available
string_desktop | Contains the build string for the desktop build, only filled when a desktop build is available. | Deprecated
string_mobile | Contains the build string for the Mobile build, only filled when a Mobile build is available. | Deprecated
string_xbox | Contains the build string for the Xbox build, only filled when a Xbox build is available. | Deprecated
string_iot | Contains the build string for the IoT build, only filled when a IoT build is available. | Deprecated
string_server | Contains the build string for the Server build, only filled when a Server build is available. | Deprecated
string_holographic | Contains the build string for the holographic build, only filled when a holographic build is available. | Deprecated
fast_desktop | Fast Ring release for desktop build. | Deprecated
slow_desktop | Slow Ring release for desktop build. | Deprecated
current_desktop | Current Branch release for desktop build. | Deprecated
business_desktop | Current Branch for Business release for desktop build. | Deprecated
ltsb_desktop | Long-Term Support Branch release for desktop build. | Deprecated
fast_mobile | Fast Ring release for Mobile build. | Deprecated
slow_mobile | Slow Ring release for Mobile build. | Deprecated
current_mobile | Current Branch release for mobile build. | Deprecated
preview_xbox | Preview release for Xbox build. | Deprecated
release_xbox | Stable release for Xbox build. | Deprecated
preview_iot | Preview release for IoT build. | Deprecated
release_iot | Stable release for IoT build. | Deprecated
preview_server | Preview release for Server build. | Deprecated
release_server | Stable release for Server build. | Deprecated
preview_holographic | Preview release for Holographic build. | Deprecated
release_holographic | Stable release for Holographic build. | Deprecated
minilog_desktop | The minilog contains a quick overview for everything new in this build for the desktop. | Deprecated
minilog_mobile | The minilog contains a quick overview for everything new in this build for Mobile. | Deprecated
minilog_xbox | The minilog contains a quick overview for everything new in this build for Xbox. | Deprecated
minilog_iot | The minilog contains a quick overview for everything new in this build for IoT. | Deprecated
minilog_server | The minilog contains a quick overview for everything new in this build for Server. | Deprecated
minilog_holographic | The minilog contains a quick overview for everything new in this build for Holographic. | Deprecated
announcement_desktop | The url to Microsofts official announcement of this build for desktop. | Deprecated
announcement_mobile | The url to Microsofts official announcement of this build for Mobile. | Deprecated
announcement_xbox | The url to Microsofts official announcement of this build for Xbox. | Deprecated
announcement_iot | The url to Microsofts official announcement of this build for IoT. | Deprecated
announcement_server | The url to Microsofts official announcement of this build for Server. | Deprecated
announcement_holographic | The url to Microsofts official announcement of this build for Holographic. | Deprecated

## Releases
**releases** contains all information regarding each individual release. One release is added for each individual ring a build has been released to. So for example, patches for 10240 are released for the Current Branch, Current Branch for Business and Long-Term Support Branch, this means that there are 3 releases with the same data but another ring.
[JSON](http://changewindows.org/api/cw/releases.json) &middot; [XML](http://changewindows.org/api/cw/releases.xml) &middot; [HTML](http://changewindows.org/api/cw/releases.html)

Field | Description | Status
------------ | ------------- | -------------
id | **Primary key**, contains the id of the release | To be added
build | Contains the build number of the release | To be added
string | Contains the string of the release | To be added
platform | Contains an integer from 1 to 6 to represent the platform (in order: desktop, Mobile, Xbox, Server, Holographic, IoT) | To be added
ring | Contains an integer from 1 to 6 to represent the branch (in order: Fast, Slow/Preview, Release Preview, Current/Release, Business, LTSB) | To be added
date | Contains the date on which the release was released | To be added
announcement | Contains an URL to the announcement of the release or to the KB article on Microsoft.com | To be added

## Rings
**rings** contains all information regarding which build is in which ring. This table is still being maintained but will cease to exist for ChangeWindows 3.0, this table will be replaced with the **releases**-table whre you simply need to pick the last release from a platform in a certain ring.
[JSON](http://changewindows.org/api/cw/rings.json) &middot; [XML](http://changewindows.org/api/cw/rings.xml) &middot; [HTML](http://changewindows.org/api/cw/rings.html)

Field | Description | Status
------------ | ------------- | -------------
id | **Primary key**, always 1. | Deprecated
fast_desktop | Fast Ring release for desktop build. | Deprecated
slow_desktop | Slow Ring release for desktop build. | Deprecated
preview_desktop | Release Preview Ring release for desktop build. | Deprecated
current_desktop | Current Branch release for desktop build. | Deprecated
business_desktop | Current Branch for Business release for desktop build. | Deprecated
ltsb_desktop | Long-Term Support Branch release for desktop build. | Deprecated
fast_mobile | Fast Ring release for Mobile build. | Deprecated
slow_mobile | Slow Ring release for Mobile build. | Deprecated
preview_mobile | Release Preview Ring release for Mobile build. | Deprecated
current_mobile | Current Branch release for mobile build. | Deprecated
preview_xbox | Preview release for Xbox build. | Deprecated
release_xbox | Stable release for Xbox build. | Deprecated
preview_iot | Preview release for IoT build. | Deprecated
release_iot | Stable release for IoT build. | Deprecated
preview_server | Preview release for Server build. | Deprecated
release_server | Stable release for Server build. | Deprecated
preview_holographic | Preview release for Holographic build. | Deprecated
release_holographic | Stable release for Holographic build. | Deprecated
fast_desktop_date | Fast Ring release date for desktop build. | Deprecated
slow_desktop_date | Slow Ring release date for desktop build. | Deprecated
preview_desktop_date | Release Preview Ring release date for desktop build. | Deprecated
current_desktop_date | Current Branch release date for desktop build. | Deprecated
business_desktop_date | Current Branch for Business release date for desktop build. | Deprecated
ltsb_desktop_date | Long-Term Support Branch release date for desktop build. | Deprecated
fast_mobile_date | Fast Ring release date for Mobile build. | Deprecated
slow_mobile_date | Slow Ring release date for Mobile build. | Deprecated
preview_mobile_date | Release Preview Ring release date for Mobile build. | Deprecated
current_mobile_date | Current Branch release date for mobile build. | Deprecated
preview_xbox_date | Preview release date for Xbox build. | Deprecated
release_xbox_date | Stable release date for Xbox build. | Deprecated
preview_iot_date | Preview release date for IoT build. | Deprecated
release_iot_date | Stable release date for IoT build. | Deprecated
preview_server_date | Preview release date for Server build. | Deprecated
release_server_date | Stable release date for Server build. | Deprecated
preview_holographic_date | Preview release date for Holographic build. | Deprecated
release_holographic_date | Stable release date for Holographic build. | Deprecated

## Milestones
**milestones** contains all information regarding milestones, e.g. Threshold 1, Threshold 2 and Redstone 1.
[JSON](http://changewindows.org/api/cw/milestones.json) &middot; [XML](http://changewindows.org/api/cw/milestones.xml) &middot; [HTML](http://changewindows.org/api/cw/milestones.html)

Field | Description | Status
------------ | ------------- | -------------
id | **Primary key**, identifies a milestone (e.g. 'redstone1'). | Available
name | Official name of the milestone (e.g. 'Anniversary Update'). | Available
version | Version number of the milestone (e.g. '1607'). | Available
osname | Contain the name of the OS (e.g. 'Window 10'). | Available
codename | The official codename used within Microsoft (e.g. 'Redstone 1') | Available
description | A description of the milestone. | Available
desktop | Contains the name for the desktop build, in addition to the basic naming. | Available
mobile | Contains the name for the Mobile build, in addition to the basic naming. | Available
xbox | Contains the name for the Xbox build, in addition to the basic naming. | Available
iot | Contains the name for the IoT build, in addition to the basic naming. | Available
server | Contains the name for the Server build, in addition to the basic naming. | Available
holographic | Contains the name for the holographic build, in addition to the basic naming. | Available