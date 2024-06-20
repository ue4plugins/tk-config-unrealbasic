[![Build Status](https://dev.azure.com/shotgun-ecosystem/Toolkit/_apis/build/status/Configs/tk-config-basic?branchName=master)](https://dev.azure.com/shotgun-ecosystem/Toolkit/_build/latest?definitionId=40&branchName=master)

-------------------------------------------------------------------------
Configuration for running ShotGrid with the Unreal Engine
-------------------------------------------------------------------------

This Toolkit configuration was forked from [tk-config-basic](https://github.com/shotgunsoftware/tk-config-basic) and updates
from that configuration are regularly merged in.

This configuration extends the tk-config-basic configuration with an 
Unreal engine as well as several Unreal related options in Maya.

For more information on how to use the Unreal engine, please see the support
documentation:

https://docs.unrealengine.com/5.0/en-US/using-unreal-engine-with-autodesk-shotgrid/

-------------------------------------------------------------------------

## Updating this config with changes from the ShotGrid basic config

It is possible to update this config with latest changes done on the ShotGrid basic config, for example
to update Shotgun Toolkit standard apps to their latest approved version.

This can be done by merging a particular ShotGrid basic config into a branch and merging this branch once checked on master

* Add ShotGrid basic config repo as a remote:  `git remote add sgbasic git@github.com:shotgunsoftware/tk-config-basic.git`
* Fetch latest changes for the ShotGrid basic config repo:  `git fetch sgbasic master`
* You can checkout these changes in a branch to check logs and tags:  `git checkout sgbasic/master`
* If needed you can keep this branch around with: `git switch -c sgmaster`
* Create a new merge branch from the master branch: `git checkout -b basic_merge`
* Merge a particular tag on this branch: `git merge v1.3.11`.
* A regular merge needs to be used to preserve tags from the ShotGrid basic config.
* Fix conflicts if any, commit and review changes.
* Merge approved changes on master, tag the internal release, push changes and the tags: `git push; git push --tags`.

The convention used so far when tagging releases for this config is `<ShotGrid basic config release>-unreal.<internal release>` 
For example `v1.3.11-unreal.0.2.6`
