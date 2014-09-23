Summary
-------
This project builds a jetty distribution containing a geoserver and mapfish-print and runs end-to-end/integration tests.

Many of the tests are examples and are ran to verify that all the examples continue to be up-to-date and give the correct response.

This module is part of the normal build process and `.gradlew build` will build and test the distribution archive.  The archive
is in `build/dists/`.

To run the tests one can execute: `./gradlew examples:test`.

If one is developing tests or debugging tests/examples then run: `./gradlew examples:jettyRun`.

To run jetty in debug mode simply execute: `./gradlew -DdebugJetty=true examples:jettyRun` and the server will be run with a debug port open on
port 5005.  To run with a different debug port execute instead: `./gradlew -DdebugJettyPort=8000 examples:jettyRun` (where 8000 can be any port you like.

The debugJetty and debugJettyPort system parameters also apply when running examples:test.
