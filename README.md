<!--
#
# Licensed to the Apache Software Foundation (ASF) under one
# or more contributor license agreements.  See the NOTICE file
# distributed with this work for additional information
# regarding copyright ownership.  The ASF licenses this file
# to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance
# with the License.  You may obtain a copy of the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
#  KIND, either express or implied.  See the License for the
# specific language governing permissions and limitations
# under the License.
#
-->

[![Build status](https://ci.appveyor.com/api/projects/status/wxkmo0jalsr8gane?svg=true)](https://ci.appveyor.com/project/ApacheSoftwareFoundation/cordova-fetch/branch/master)
[![Build Status](https://travis-ci.org/apache/cordova-fetch.svg?branch=master)](https://travis-ci.org/apache/cordova-fetch)
[![NPM](https://nodei.co/npm/cordova-fetch.png)](https://nodei.co/npm/cordova-fetch/)

# cordova-fetch

This module is used for fetching modules from npm and gitURLs. It fetches the modules via `npm install`. It can also `npm uninstall` modules from a project.

## Usage:

### Fetching:
```
var fetch = require('cordova-fetch');

fetch(spec, dest, opts);
```

`spec` can be a string containg a npm `packageID` or a `git URL`. 
`dest` is string of the directory location you wish to `npm install` these modules.
`opts` is an Object of options cordova fetch handles. Currently, fetch only support the `save` option.
    eg. `{'save':true}`

### Removing:
```
var npmUninstall = require('cordova-fetch').uninstall;

npmUninstall(spec, dest, opts);
```

`spec` can be a string containg a npm `packageID`. 
`dest` is string of the directory location you wish to `npm uninstall` these modules.
`opts` is an Object of options cordova fetch handles. Currently, fetch only support the `save` option.
    eg. `{'save':true}`
