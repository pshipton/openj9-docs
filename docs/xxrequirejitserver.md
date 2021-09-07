<!--
* Copyright (c) 2021, 2021 IBM Corp. and others
*
* This program and the accompanying materials are made
* available under the terms of the Eclipse Public License 2.0
* which accompanies this distribution and is available at
* https://www.eclipse.org/legal/epl-2.0/ or the Apache
* License, Version 2.0 which accompanies this distribution and
* is available at https://www.apache.org/licenses/LICENSE-2.0.
*
* This Source Code may also be made available under the
* following Secondary Licenses when the conditions for such
* availability set forth in the Eclipse Public License, v. 2.0
* are satisfied: GNU General Public License, version 2 with
* the GNU Classpath Exception [1] and GNU General Public
* License, version 2 with the OpenJDK Assembly Exception [2].
*
* [1] https://www.gnu.org/software/classpath/license.html
* [2] http://openjdk.java.net/legal/assembly-exception.html
*
* SPDX-License-Identifier: EPL-2.0 OR Apache-2.0 OR GPL-2.0 WITH
* Classpath-exception-2.0 OR LicenseRef-GPL-2.0 WITH Assembly-exception
-->

# -XX:\[+|-\]RequireJITServer

When you enable this option, JITServer client will crash with an assert if it detects that a server is unavailable.

## Syntax

        -XX:[+|-]RequireJITServer

| Setting                 | Effect | Default                                                                            |
|-------------------------|--------|:----------------------------------------------------------------------------------:|
|`-XX:+RequireJITServer`           | Enable |                                                                                    |
|`-XX:-RequireJITServer`           | Disable| :fontawesome-solid-check:{: .yes aria-hidden="true"}<span class="sr-only">yes</span> |

## Explanation

This option is for debugging purposes only.

Without this option, a server crash will force the client to perform compilations locally. However, when running a test suite with JITServer enabled, you might want to use this option. It will cause a test to fail if the server crashes, instead of switching to local compilations and hiding the failure.

<!-- ==== END OF TOPIC ==== xxrequirejitserver.md ==== -->