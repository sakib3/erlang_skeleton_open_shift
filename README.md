erlcart
=======

This effort aims to create convenient support for Erlang web server for redhat's OpenShift. Development is easier due to OpenShift's scaling, automated builds and deployment but also limits the structure and usage of application.

Exhaustive documentation on www.openshift.com provides essential information for usage and deployment. Few additional steps required by erlang cartridge are described below.

#### What this cartridge currently offers?

- Erlang/OTP 18.2.1 - pre-build
- rebar & rebar3 - tool for application build
- elixir v1.2

#### What it supports?

Currently cartridge has been tested with [Cowboy web server](https://github.com/ninenines/cowboy), thanks to uniform OTP development and file structure, it is assumed that any web server following OTP principles is supported as well.

#### How do I create the application?

Create the application in [OpenShift](www.openshift.com), add [manifest](https://raw.githubusercontent.com/wozniakjan/erlcart/master/metadata/manifest.yml) from this repository, clone applications repository and push your OTP application's code. The cartridge will take care of automated build and deployment. In case you are not familiar with Cowboy and web development in OTP, there is barebone app created for your convenience in
[/template/](https://github.com/wozniakjan/erlcart/tree/master/template).

    rhc create-app erlapp https://raw.githubusercontent.com/wozniakjan/erlcart/master/metadata/manifest.yml

#### Are there any examples running around?

Apart from others, there are two apps running:

1) [test](http://hello-wozj.rhcloud.com/) application from [/template/](https://github.com/wozniakjan/erlcart/tree/master/template)


2) [camchat](https://camchat.herokuapp.com/) HTML5 based web video conference (which is more proof of concept than actuall application, work is in progress and far from being finished, but hopefully testable)

#### That's it?
yep.
