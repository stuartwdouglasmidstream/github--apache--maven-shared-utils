<!---
Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
KIND, either express or implied.  See the License for the
specific language governing permissions and limitations
under the License.
-->
Apache Maven Shared Utils

This project aims to be a functional replacement for
plexus-utils in maven core. It is not a 100% API compatible
replacement though. Lots of methods got cleaned up, generics
got added and we dropped a lot of unused code.


Relation to Commons-*

maven-shared-utils internally use commons-io. We shade all commons
classes into our own private package to prevent classpatch clashes.
This is the reason why any public API in maven-shared-utils must
avoid to expose commons classe directly. Most times it's sufficient
to just create an empty subclass and expose that instead.
