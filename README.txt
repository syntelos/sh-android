
Android build script for linux


Synopsis

    android

Description

    This script encapsulates the android build process.

Status

    Work in progress.

Design

    Unanticipated variations in project organization (directory
    structure and file location) are solved by configuration.  

    Refer to the documentation more more information.

Documentation

    Invoking

        2>&1 android -? | less

    will pipe the help text to the 'less' pager.

Installation

    Prerequisites

	The home 'bin' directory (${HOME}/bin) must exist, and must be
	in the PATH, and its position in the PATH must be superior to
	the 'android-sdk/tools' directory (where google's deprecated
	'android' script is located).

    Synopsis

        ./install; echo $?

    Description

	This will attempt to copy the "android" shell script to
	'${HOME}/bin', and to validate the installation.

    Results

	The installation script will fail (result code "1", not "0")
	when '${HOME}/bin' is not found, or 'which android' is not
	'${HOME}/bin/android'.  The installation will also fail when
	the 'which' program is not (properly) installed.

Quick start

    In the root directory of a project, as (for example)

        cd ~/src/some-android-application

    Run

	android debug-install; echo $?

    If it fails, the design intent is to remedy the situation by
    testing, probing, and configuration.


Caveats

    This script (creates and) destroys application project (working
    directory) [sub] directories 'obj' and 'bin'.

Credits

    Written with the recipe found in...

    "How to make Android apps without IDE from command line"
    https://medium.com/@authmane512/how-to-build-an-apk-from-command-line-without-ide-7260e1e22676

    by Authmane Terki, https://medium.com/@authmane512
                       https://github.com/authmane512
