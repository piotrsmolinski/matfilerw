# <img align="left" src="matfilerw.png"> MatFileRW: Read and write MATLAB MAT-files from Java

<!---freshmark shields
output = [
	link(shield('Maven artifact', 'mavenCentral', '{{group}}:{{name}}', 'blue'), 'https://bintray.com/{{org}}/opensource/{{name}}/view'),
	link(shield('Latest version', 'latest', '{{stable}}', 'blue'), 'https://github.com/{{org}}/{{name}}/releases/latest'),
	link(shield('Javadoc', 'javadoc', 'OK', 'blue'), 'https://{{org}}.github.io/{{name}}/javadoc/{{stable}}/'),
	link(shield('License Apache', 'license', 'BSD', 'blue'), 'https://tldrlegal.com/license/bsd-3-clause-license-(revised)'),
	'',
	link(shield('Changelog', 'changelog', '{{version}}', 'brightgreen'), 'CHANGES.md'),
	link(image('Travis CI', 'https://travis-ci.org/{{org}}/{{name}}.svg?branch=master'), 'https://travis-ci.org/{{org}}/{{name}}')
	].join('\n');
-->
[![Maven artifact](https://img.shields.io/badge/mavenCentral-com.diffplug.matsim%3Amatfilerw-blue.svg)](https://bintray.com/diffplug/opensource/matfilerw/view)
[![Latest version](https://img.shields.io/badge/latest-1.2.0-blue.svg)](https://github.com/diffplug/matfilerw/releases/latest)
[![Javadoc](https://img.shields.io/badge/javadoc-OK-blue.svg)](https://diffplug.github.io/matfilerw/javadoc/1.2.0/)
[![License Apache](https://img.shields.io/badge/license-BSD-blue.svg)](https://tldrlegal.com/license/bsd-3-clause-license-(revised))

[![Changelog](https://img.shields.io/badge/changelog-1.3.0--SNAPSHOT-brightgreen.svg)](CHANGES.md)
[![Travis CI](https://travis-ci.org/diffplug/matfilerw.svg?branch=master)](https://travis-ci.org/diffplug/matfilerw)
<!---freshmark /shields -->

JMatIO is a library which allows reading and writing MAT files.  Have a look at [MatIOTest.java](src/test/java/com/jmatio/test/MatIOTest.java?ts=4) to see each part in use.

As far as compatibility, the TL;DR is that it will work with any MAT-File with default settings.  The dirty details are that this library works with `v6` and `v7`, but not `v4` or `v7.3`.

* v4 is the default format before R8
* v6 is the default format from R8 to R13
* v7 is the default format from R14 to present (every R20XXX release)
* MATLAB does not export to v7.3 by default.
* The [Mathworks website](http://www.mathworks.com/help/matlab/import_export/mat-file-versions.html?refresh=true) has more details.

## Acknowledgements

This project is forked from the JMatIO project originally maintained on [SourceForge](http://sourceforge.net/projects/jmatio/), and now maintained on [GitHub](https://github.com/gradusnikov/jmatio).  The name was changed to ensure that we don't infringe the original project's license, but we did not change the package names, so this project is binary compatible with the original JMatIO.  This fork is in no way associated with or endorsed by any authors of the original project.

We have fixed some bugs and added some features (see the [changelog](CHANGES.md)), and we will maintain this library into the future.  We're happy to accept pull requests](CONTRIBUTING.md) too!

* Formatted by [spotless](https://github.com/diffplug/spotless), [as such](https://github.com/diffplug/durian-rx/blob/v1.0/build.gradle?ts=4#L70-L90).
* Bugs found by [findbugs](http://findbugs.sourceforge.net/), [as such](https://github.com/diffplug/durian-rx/blob/v1.0/build.gradle?ts=4#L92-L116).
* OSGi metadata generated by JRuyi's [osgibnd-gradle-plugin] (https://github.com/jruyi/osgibnd-gradle-plugin), which leverages Peter Kriens' [bnd](http://www.aqute.biz/Bnd/Bnd).
* Scripts in the `.ci` folder are inspired by [Ben Limmer's work](http://benlimmer.com/2013/12/26/automatically-publish-javadoc-to-gh-pages-with-travis-ci/).
* Built by [gradle](http://gradle.org/).
* Tested by [junit](http://junit.org/).
* Maintained by [DiffPlug](http://www.diffplug.com/).
