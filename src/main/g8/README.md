## $name$ - performance test suite

Project uses [sbt plugin][sbtplugindoc] of [gatling][gatlingdoc].
It contains basic simulation from gatling quick start bundle.

[sbtplugindoc]: https://gatling.io/docs/current/extensions/sbt_plugin/
[gatlingdoc]: https://gatling.io/docs/current/advanced_tutorial/

### Run

All tests:
```
sbt "gatling:test"
```

Single test:
```
sbt "gatling:testOnly computerdatabase.BasicSimulation"
```

Report:
```
sbt "gatling:lastReport"
```

### JAR

Build:
```
sbt "test:assembly"
```

Run:
```
java -jar target/scala-2.12/$name$-test-0.1.0-SNAPSHOT.jar -s computerdatabase.BasicSimulation
```

The path to report will be printed at the end of the run, like this:
```
Reports generated in 0s.
Please open the following file: /Users/spikerlabs/gatling/results/basicsimulation-1535151426929/index.html
```
