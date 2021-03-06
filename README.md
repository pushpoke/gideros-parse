gideros-parse
=============

# Parse integration for Gideros using BhWax

This module provides social integration code for using the Parse SDK with Gideros, via BhWax.

You will need to have both BhWax (the very latest) and the Parse SDK for iOS setup for use with the Gidero iOS Player.

##Installation and Setup

###1) BhWax:
Wax (https://github.com/probablycorey/wax) is a Lua <-> Objective C bridge by Corey Johnson. A modified version of this for
use with Gideros (http://giderosmobile.com) was developed by Andy Bower called BhWax (https://github.com/bowerhaus/BhWax). 

You can read more about BhWax, including instructions on how to build the plugin, on Andy's blog post 
(http://bowerhaus.eu/blog/files/hot_wax.html).

a) Install BhWax as per the instructions on http://bowerhaus.eu/blog/files/hot_wax.html

b) You will need to update to the BhWax.mm included here. This includes additional Block functions you'll need.

###2) Parse SDK for iOS:
a) Sign up at http://parse.com/

b) Follow the quick start guide provided by Parse (https://www.parse.com/apps/quickstart)

 - Select iOS, existing project, your app from downdown.

c) Add the following to ProtocolLoader.h (from BhWax):

	@protocol(PFLogInViewControllerDelegate) &&
	@protocol(PFSignUpViewControllerDelegate) &&

d) Note you should additionally set the XCode > Target > Build Settings > Other Linker Flags to use "-all_load -ObjC"

e) To confirm Parse is setup properly, run ParseLib:test(), then confirm on the Parse web site checker

###3) [optional] Setup Facebook and Twitter authentication

a) Setup a Facebook application and add your App ID in "fbAppId" near the top of main.lua

b) Setup a Twitter application and add your consumer key and secret in "twitKey" and "twitSecret" near the top of main.lua

##Usage

See main.lua for thorough implementation example.
	
