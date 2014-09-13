HubFlow (WebSharks Flavor)
=======

Adds the 'git hf' Git extension to provide high-level repository operations
for [DataSift's HubFlow branching model](http://datasift.github.com/gitflow/), which is based on [Vincent Driessen’s original blog post](http://nvie.com/posts/a-successful-git-branching-model/). See also: [WebSharks Flavor Changes](https://github.com/websharks/hubflow/blob/000000-dev/README.md#websharks-flavor-changes).

![](http://nvie.com/img/2009/12/Screen-shot-2009-12-24-at-11.32.03.png)

![](https://cloud.githubusercontent.com/assets/53005/3305294/37040e0e-f654-11e3-8042-ae18b34891b7.png)

Installation (WebSharks Flavor)
------------

#### Mac via [Homebrew](http://brew.sh/) (recommended)

```
brew tap websharks/homebrew-hubflow-ws
brew install hubflow-ws
```

#### All Other Operating Systems

1. `git clone https://github.com/websharks/hubflow.git`
2. `cd hubflow` && `git checkout master`
3. `sudo ./install.sh`

Windows users will need something like Cygwin in order to use this extension.

Upgrading To The Latest Version
-------------------------------

Upgrading to the latest version of the HubFlow tools is very easy:

#### Mac via [Homebrew](http://brew.sh/) (recommended)

```
brew update
brew upgrade hubflow-ws
```

#### All Other Operating Systems

1. `sudo git hf upgrade`

Getting Started
---------------

See our tutorial website to learn more about the [GitFlow](http://datasift.github.com/gitflow/IntroducingGitFlow.html) branching model and [how to use the HubFlow tools](http://datasift.github.com/gitflow/GitFlowForGitHub.html).

Changelog
---------

To see what's new in each release, see our [Changelog](http://datasift.github.com/gitflow/ChangeLog.html).

WebSharks Flavor Changes
-----------------------

- Added support for an additional synchronized repo that rides with the primary.
- Added a scan for an existing `000000-dev` branch; if it exists we use this over the default name: `develop` for the "next release" branch.

### Repo Synchronization

**To enable the synchronization functionality** (i.e. if you have both a lite/pro version you are maintaining together); use the `s` flag.

#### Example...

From your repo directory...
```
$ git hf init -asf
```

#### Usage...

From your repo directory...
```
$ git hf init -asf
```
... just fill in the blanks where it asks for your configuration. Most of it can just be left with the default values. To clarify, there are three flags here. `a` = ask for configuration values, `s` = enable synchronization functionality (optional), and `f` = force a new set of config values, overriding any that already exist. I recommend always using these flags together; i.e. `git hf init -asf`

**NOTE:** If you enable the `s` flag (synchronization) you will be asked for two config sets. That's normal. In synchronization mode all of your commands are duplicated across two repos.

Once you are configured, you can do this...

```
$ git hf feature start 123
```

... where `123` is a GitHub issue that is connected to a feature branch.

License Terms
-------------
HubFlow is published under the liberal terms of the BSD License, see the
[LICENSE](LICENSE) file. Although the BSD License does not require you to share
any modifications you make to the source code, you are very much encouraged and
invited to contribute back your modifications to the community, preferably
in a Github fork, of course.

---

This project is now on Floobits too! [Watch us code](https://floobits.com/jaswsinc/hubflow/redirect) in real-time :-) <a href="https://floobits.com/jaswsinc/hubflow/redirect"><img alt="Floobits status" width="100" height="40" src="https://floobits.com/jaswsinc/hubflow.png" align="right" /></a>
