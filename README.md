<!--

    Sonatype Nexus (TM) Open Source Version
    Copyright (c) ${currentYear}-present Sonatype, Inc.
    All rights reserved. Includes the third-party code listed at http://links.sonatype.com/products/nexus/oss/attributions.

    This program and the accompanying materials are made available under the terms of the Eclipse Public License Version 1.0,
    which accompanies this distribution and is available at http://www.eclipse.org/legal/epl-v10.html.

    Sonatype Nexus (TM) Professional Version is available from Sonatype, Inc. "Sonatype" and "Sonatype Nexus" are trademarks
    of Sonatype, Inc. Apache Maven is a trademark of the Apache Software Foundation. M2eclipse is a trademark of the
    Eclipse Foundation. All other trademarks are the property of their respective owners.

-->
# CircleCI Maven Release Orb [![CircleCI Build Status](https://circleci.com/gh/sonatype-nexus-community/circleci-maven-release-orb.svg?style=shield "CircleCI Build Status")](https://circleci.com/gh/sonatype-nexus-community/circleci-maven-release-orb) [![CircleCI Orb Version](https://img.shields.io/badge/endpoint.svg?url=https://badges.circleci.io/orb/sonatype-nexus-community/circleci-maven-release-orb)](https://circleci.com/orbs/registry/orb/sonatype-nexus-community/circleci-maven-release-orb) [![GitHub License](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/sonatype-nexus-community/circleci-maven-release-orb/master/LICENSE) [![CircleCI Community](https://img.shields.io/badge/community-CircleCI%20Discuss-343434.svg)](https://discuss.circleci.com/c/ecosystem/orbs)

[![CircleCI](https://circleci.com/gh/sonatype-nexus-community/circleci-maven-release-orb.svg?style=svg)](https://circleci.com/gh/sonatype-nexus-community/circleci-maven-release-orb)

A CircleCI [Orb](https://circleci.com/docs/2.0/orb-intro/) than can be used to deploy maven projects using the [maven-release-plugin](https://maven.apache.org/maven-release/maven-release-plugin/).

Click the `orb version` badge above for usage examples and documentation.

<!--
 TODO: add demo project to community
See the [demo](https://github.com/sonatype-nexus-community-circleci/circleci-maven-release-orb-demo) on the Sonatype Community site for a working example.
-->
#### How to use the Maven Release Orb in your config.yml

There are a number of examples in the Orb documentation 
(see the [Example source code](https://github.com/sonatype-nexus-community/circleci-maven-release-orb/blob/master/src/orb.yml#L104)).

The [simplest example](https://github.com/sonatype-nexus-community/circleci-maven-release-orb/blob/master/src/orb.yml#L105)
 of a CircleCI `config.yml` file is duplicated below:

      version: 2.1

      orbs:
        circleci-maven-release-orb: sonatype-nexus-community/circleci-maven-release-orb@x.y.z

      workflows:
        main:
          jobs:
            - circleci-maven-release-orb/run-maven-release

You would replace `x.y.z` with a real version.
To use the latest development version of the Orb, replace `x.y.z` with `dev:alpha`.

While experimenting with this plugin, you should use the 
[Dry Run example](https://github.com/sonatype-nexus-community/circleci-maven-release-orb/blob/master/src/orb.yml#L118) 
to avoid creating a bunch of spurious releases.

The [Orb Description section](https://github.com/sonatype-nexus-community/circleci-maven-release-orb/blob/master/src/orb.yml#L2) 
documents additional requirements for using this Orb.
 
## The Fine Print

It is worth noting that this is **NOT SUPPORTED** by Sonatype, and is a contribution of ours
to the open source community (read: you!)

Don't worry, using this community item does not "void your warranty". In a worst case scenario, you may be asked 
by the Sonatype Support team to remove the community item in order to determine the root cause of any issues.

Remember:

* Use this contribution at the risk tolerance that you have
* Do NOT file Sonatype support tickets related to Orb support
* DO file issues here on GitHub, so that the community can pitch in

Phew, that was easier than I thought. Last but not least of all:

Have fun creating and using this Orb, we are glad to have you here!

## Getting help

Looking to contribute to our code but need some help? There's a few ways to get information:

* Chat with us on [Gitter](https://gitter.im/sonatype/nexus-developers)
* See the `community: CircleCI Discuss` badge at the top of this page.
