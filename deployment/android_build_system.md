## Artifact:
An artifact is the outcome of any process.
In android apk or aab is the outcome of build process, so they are reffered to as build artifact.

## Build Types:
It defines how the aab or apk should be built. 

For e.g. Whther an apk should enable debug and ligging option is generally determined by its build type. If an apk is built with debug build type then debugging and logging option will be enabled. Or if it were built with release build type then it would be shrinked and obfuscated, optimized for performance, signed with special key etc.

Commonly there are three build types:- debug, release and profile.

Note: Profile build is used for performance tunning of any app. 

## Build variants: 
As documentation staes 'Its the cross-product of build type and product flavor'. 

For e.g. Let say, there is aa app that has 2 product flavor 1. Free 2. Premium. 

Let say, It also has 2 built types 1. debug and 2. release

Then the app will have 4 build variant.

1. freeDebug
2. freeRelease
3. premiumDebug
4. premiumRelease