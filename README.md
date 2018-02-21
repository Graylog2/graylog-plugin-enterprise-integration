# DEPRECATION NOTICE

This project has been merged into [graylog2-server](https://github.com/Graylog2/graylog2-server), see [#10](https://github.com/Graylog2/graylog-plugin-enterprise-integration/issues/10)

Please use the [issue tracker in the graylog2-server repository](https://github.com/Graylog2/graylog2-server/issues) for any feature requests or bug reports.

----

# Enterprise Integration Plugin for Graylog

Plugin that provides basic integration with Graylog Enterprise.

**Required Graylog version:** 2.0 and later

Installation
------------

[Download the plugin](https://github.com/Graylog2/graylog-plugin-enterprise-integration/releases)
and place the `.jar` file in your Graylog plugin directory. The plugin directory
is the `plugins/` folder relative from your `graylog-server` directory by default
and can be configured in your `graylog.conf` file.

Restart `graylog-server` and you are done.

Development
-----------

You can improve your development experience for the web interface part of your plugin
dramatically by making use of hot reloading. To do this, do the following:

* `git clone https://github.com/Graylog2/graylog2-server.git`
* `cd graylog2-server/graylog2-web-interface`
* `ln -s $YOURPLUGIN plugin/`
* `npm install && npm start`


Getting started
---------------

This project is using Maven 3 and requires Java 7 or higher.

* Clone this repository.
* Run `mvn package` to build a JAR file.
* Optional: Run `mvn jdeb:jdeb` and `mvn rpm:rpm` to create a DEB and RPM package respectively.
* Copy generated JAR file in target directory to your Graylog plugin directory.
* Restart the Graylog.

Plugin Release
--------------

We are using the maven release plugin:

```
$ mvn release:prepare
[...]
$ mvn release:perform
```

This sets the version numbers, creates a tag and pushes to GitHub. Travis CI will build the release artifacts and upload to GitHub automatically.
