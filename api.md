# ChangeWindows.org API
We provide some of our data with an API, this includes build information, ring information and milestone information. All tables are available as JSON, XML and HTML.

## Builds
**builds** contains all information about every single build. This includes build strings, minilogs, release dates and announcement urls.
[JSON](http://changewindows.org/api/cw/builds.json) &middot; [XML](http://changewindows.org/api/cw/builds.xml) &middot; [HTML](http://changewindows.org/api/cw/builds.html)

Field | Description | Status
------------ | ------------- | -------------
build | **Primary key**, contains the build number. | Available
string_desktop | Contains the build string for the desktop build, only filled when a desktop build is available. | Available
string_mobile | Contains the build string for the Mobile build, only filled when a Mobile build is available. | Available
string_xbox | Contains the build string for the Xbox build, only filled when a Xbox build is available. | Available
string_iot | Contains the build string for the IoT build, only filled when a IoT build is available. | Available
string_server | Contains the build string for the Server build, only filled when a Server build is available. | Available
string_holographic | Contains the build string for the holographic build, only filled when a holographic build is available. | Available
version | The version number (e.g. 1507, 1511, 1607). | Deprecated
name_desktop | Contains the name for the desktop build, in addition to the basic naming. | Available
name_mobile | Contains the name for the Mobile build, in addition to the basic naming. | Available
name_xbox | Contains the name for the Xbox build, in addition to the basic naming. | Available
name_iot | Contains the name for the IoT build, in addition to the basic naming. | Available
name_server | Contains the name for the Server build, in addition to the basic naming. | Available
name_holographic | Contains the name for the holographic build, in addition to the basic naming. | Available
fast_desktop | Fast Ring release for desktop build. | Available
slow_desktop | Slow Ring release for desktop build. | Available
current_desktop | Current Branch release for desktop build. | Available
business_desktop | Current Branch for Business release for desktop build. | Available
ltsb_desktop | Long-Term Support Branch release for desktop build. | Available
fast_mobile | Fast Ring release for Mobile build. | Available
slow_mobile | Slow Ring release for Mobile build. | Available
current_mobile | Current Branch release for mobile build. | Available
preview_xbox | Preview release for Xbox build. | Available
release_xbox | Stable release for Xbox build. | Available
preview_iot | Preview release for IoT build. | Available
release_iot | Stable release for IoT build. | Available
preview_server | Preview release for Server build. | Available
release_server | Stable release for Server build. | Available
preview_holographic | Preview release for Holographic build. | Available
release_holographic | Stable release for Holographic build. | Available
minilog_desktop | The minilog contains a quick overview for everything new in this build for the desktop. | Available
minilog_mobile | The minilog contains a quick overview for everything new in this build for Mobile. | Available
minilog_xbox | The minilog contains a quick overview for everything new in this build for Xbox. | Available
minilog_iot | The minilog contains a quick overview for everything new in this build for IoT. | Available
minilog_server | The minilog contains a quick overview for everything new in this build for Server. | Available
minilog_holographic | The minilog contains a quick overview for everything new in this build for Holographic. | Available
announcement_desktop | The url to Microsofts official announcement of this build for desktop. | Available
announcement_mobile | The url to Microsofts official announcement of this build for Mobile. | Available
announcement_xbox | The url to Microsofts official announcement of this build for Xbox. | Available
announcement_iot | The url to Microsofts official announcement of this build for IoT. | Available
announcement_server | The url to Microsofts official announcement of this build for Server. | Available
announcement_holographic | The url to Microsofts official announcement of this build for Holographic. | Available

## Rings
**rings** contains all information regarding which build is in which ring.
[JSON](http://changewindows.org/api/cw/rings.json) &middot; [XML](http://changewindows.org/api/cw/rings.xml) &middot; [HTML](http://changewindows.org/api/cw/rings.html)

Field | Description | Status
------------ | ------------- | -------------
id | **Primary key**, always 1. | Available
fast_desktop | Fast Ring release for desktop build. | Available
slow_desktop | Slow Ring release for desktop build. | Available
preview_desktop | Release Preview Ring release for desktop build. | Available
current_desktop | Current Branch release for desktop build. | Available
business_desktop | Current Branch for Business release for desktop build. | Available
ltsb_desktop | Long-Term Support Branch release for desktop build. | Available
fast_mobile | Fast Ring release for Mobile build. | Available
slow_mobile | Slow Ring release for Mobile build. | Available
preview_mobile | Release Preview Ring release for Mobile build. | Available
current_mobile | Current Branch release for mobile build. | Available
preview_xbox | Preview release for Xbox build. | Available
release_xbox | Stable release for Xbox build. | Available
preview_iot | Preview release for IoT build. | Available
release_iot | Stable release for IoT build. | Available
preview_server | Preview release for Server build. | Available
release_server | Stable release for Server build. | Available
preview_holographic | Preview release for Holographic build. | Available
release_holographic | Stable release for Holographic build. | Available
fast_desktop_date | Fast Ring release date for desktop build. | Available
slow_desktop_date | Slow Ring release date for desktop build. | Available
preview_desktop_date | Release Preview Ring release date for desktop build. | Available
current_desktop_date | Current Branch release date for desktop build. | Available
business_desktop_date | Current Branch for Business release date for desktop build. | Available
ltsb_desktop_date | Long-Term Support Branch release date for desktop build. | Available
fast_mobile_date | Fast Ring release date for Mobile build. | Available
slow_mobile_date | Slow Ring release date for Mobile build. | Available
preview_mobile_date | Release Preview Ring release date for Mobile build. | Available
current_mobile_date | Current Branch release date for mobile build. | Available
preview_xbox_date | Preview release date for Xbox build. | Available
release_xbox_date | Stable release date for Xbox build. | Available
preview_iot_date | Preview release date for IoT build. | Available
release_iot_date | Stable release date for IoT build. | Available
preview_server_date | Preview release date for Server build. | Available
release_server_date | Stable release date for Server build. | Available
preview_holographic_date | Preview release date for Holographic build. | Available
release_holographic_date | Stable release date for Holographic build. | Available

## Milestones
**milestones** contains all information regarding milestones, e.g. Threshold 1, Threshold 2 and Redstone 1.
[JSON](http://changewindows.org/api/cw/milestones.json) &middot; [XML](http://changewindows.org/api/cw/milestones.xml) &middot; [HTML](http://changewindows.org/api/cw/milestones.html)

Field | Description | Status
------------ | ------------- | -------------
id | **Primary key**, identifies a milestone (e.g. 'redstone1'). | Available
name | Official name of the milestone (e.g. 'Anniversary Update'). | Available
version | Version number of the milestone (e.g. '1607'). | Available
first_build | First build that can be considered part of this particular milestone. | Available
last_build | Last build that can be considered part of this particular milestone. | Available
codename | The official codename used within Microsoft (e.g. 'Redstone 1') | Available
description | A description of the milestone. | Available
is_desktop | 1 if desktop, 0 if not. | Available
is_mobile | 1 if Mobile, 0 if not. | Available
is_xbox | 1 if Xbox, 0 if not. | Available
is_iot | 1 if IoT, 0 if not. | Available
is_server | 1 if Server, 0 if not. | Available
is_holographic | 1 if Holographic, 0 if not. | Available