HDPDemoStudio
============

Making HDP Demos easy


Now supporting HDP 2.3.0.0.-2577

Default mode is binary delivery now. This means HDPAppStudio is an Ambari View on it's own. 
Having said that property-files are still ok. In fact the Ambari view takes your input and creates a property-file from them.

To build HDP AppStudio run the following commands on a 2.3.0.0-2577 Sandbox or cluster:
```
$ mvn clean compile assembly:single
$ cd StormTopology
$ mvn clean compile assembly:single
$ cd SparkStreaming
$ mvn clean compile assembly:single
$ cd ..
$ ./createpkg.sh
```

This will produce a tar-ball under ``dist/``.

Copy the tar-ball dist/HDPDemoStudio-bin-*.tar on the a fresh Sandbox
and run: 
    $ tar xf HDPAppStudio-bin-*.tar
    $ ./install.sh

Afterwards find your HDPAppStudio View in Ambari and create your application there. 
 
Alternatively you start a fresh sandbox, logon and do:
```
$ git clone https://github.com/digitalemil/HDPDemoStudio.git
$ cd HDPDemoStudio
$ sh ./install.sh
```
and follow the output



