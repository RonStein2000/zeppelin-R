# Apache Zeppelin R Interpreter

This is a interperter for [R](http://cran.r-project.org) code for the [Apache Zeppelin notebook](http://zeppelin.incubator.apache.org).

[![R Interpreter Screenshot](http://datalayer.io/ext/screenshots/R-interpreter.png)](http://datalayer.io)

It support cross paragraph variables and R plot (ggplot2...).

Due to GPL2 license of used libraries, this software is not released under ASL2 ([read more](http://www.apache.org/foundation/license-faq.html#GPL)).

# Prerequisite

You need to have R (with Rserve and knitr) available on the host running the notebook.

For Centos: `yum install R R-devel`

For Ubuntu: `apt-get install r-base r-cran-rserve`

Launch R command and install the needed packages:

```
install.packages("Rserve")
install.packages("knitr")
```

# Build

```
mvn install
```

# Integrate in Apache Zeppelin

We depend on [ZEPPELIN-154 - Load Interpreter via Classpath](https://issues.apache.org/jira/browse/ZEPPELIN-154) JIRA.

Once this will be resolved, the dependency can be used in your project by declaring it with e.g. Maven:

```
<dependency>
  <groupId>io.datalayer</groupId>
  <artifactId>zeppelin-R</artifactId>
  <version>1.0.0-SNAPSHOT</version>
</dependency>
```

Optionally, you can do manual work to ship it in a Zeppelin distribution.

# Licensed under GNU General Public License

Copyright (c) 2015 Datalayer (http://datalayer.io)

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.

[![R](http://datalayer.io/ext/images/logo-R-200.png)](http://cran.r-project.org)

[![Apache Zeppelin](http://datalayer.io/ext/images/logo-zeppelin-small.png)](http://zeppelin.incubator.apache.org)

[![Datalayer](http://datalayer.io/ext/images/logo_horizontal_072ppi.png)](http://datalayer.io)
