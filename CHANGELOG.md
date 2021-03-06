# Changelog

## [v0.3.0](https://github.com/gojek/feast/tree/v0.3.0) (2019-11-19)

[Full Changelog](https://github.com/gojek/feast/compare/v0.1.8...v0.3.0)

**Summary:**

* Introduced "Feature Sets" as a concept with a new [Feast Core API](https://github.com/gojek/feast/blob/v0.3.0/protos/feast/core/CoreService.proto), [Feast Serving API](https://github.com/gojek/feast/blob/v0.3.0/protos/feast/serving/ServingService.proto)
* Upgraded [Python SDK](https://github.com/gojek/feast/tree/v0.3.0/sdk/python) to support new Feast API. Allows for management of Feast as a library or through the command line.
* Implemented a [Golang SDK](https://github.com/gojek/feast/tree/v0.3.0/sdk/go) and [Java SDK](https://github.com/gojek/feast/tree/v0.3.0/sdk/java) to support the new Feast Core and Feast Serving APIs.
* Added support for multi-feature set retrieval and joins.
* Added point-in-time correct retrieval for both batch and online serving.
* Added support for an external source in Kafka.
* Added job management to Feast Core to manage ingestion/population jobs to remote Feast deployments
* Added metric support through Prometheus

**Merged pull requests:**

- Regenerate go protos [\#313](https://github.com/gojek/feast/pull/313) ([zhilingc](https://github.com/zhilingc))
- Bump chart version to 0.3.0 [\#311](https://github.com/gojek/feast/pull/311) ([zhilingc](https://github.com/zhilingc))
- Refactored Core API: ListFeatureSets, ListStore, and GetFeatureSet [\#309](https://github.com/gojek/feast/pull/309) ([woop](https://github.com/woop))
- Use Maven's --also-make by default [\#308](https://github.com/gojek/feast/pull/308) ([ches](https://github.com/ches))
- Python SDK Ingestion and schema inference updates [\#307](https://github.com/gojek/feast/pull/307) ([woop](https://github.com/woop))
- Batch ingestion fix [\#299](https://github.com/gojek/feast/pull/299) ([zhilingc](https://github.com/zhilingc))
- Update values-demo.yaml to make Minikube installation simpler [\#298](https://github.com/gojek/feast/pull/298) ([woop](https://github.com/woop))
- Fix bug in core not setting default Kafka source [\#297](https://github.com/gojek/feast/pull/297) ([woop](https://github.com/woop))
- Replace Prometheus logging in ingestion with StatsD logging [\#293](https://github.com/gojek/feast/pull/293) ([woop](https://github.com/woop))
- Feast Core: Stage files manually when launching Dataflow jobs [\#291](https://github.com/gojek/feast/pull/291) ([davidheryanto](https://github.com/davidheryanto))
- Database tweaks [\#290](https://github.com/gojek/feast/pull/290) ([smadarasmi](https://github.com/smadarasmi))
- Feast Helm charts and build script [\#289](https://github.com/gojek/feast/pull/289) ([davidheryanto](https://github.com/davidheryanto))
- Fix max\_age changes not updating specs and add TQDM silencing flag [\#292](https://github.com/gojek/feast/pull/292) ([woop](https://github.com/woop))
- Ingestion fixes [\#286](https://github.com/gojek/feast/pull/286) ([zhilingc](https://github.com/zhilingc))
- Consolidate jobs [\#279](https://github.com/gojek/feast/pull/279) ([zhilingc](https://github.com/zhilingc))
- Import Spring Boot's dependency BOM, fix spring-boot:run at parent project level [\#276](https://github.com/gojek/feast/pull/276) ([ches](https://github.com/ches))
- Feast 0.3 Continuous Integration \(CI\) Update  [\#271](https://github.com/gojek/feast/pull/271) ([davidheryanto](https://github.com/davidheryanto))
- Add batch feature retrieval to Python SDK [\#268](https://github.com/gojek/feast/pull/268) ([woop](https://github.com/woop))
- Set Maven build requirements and some project POM metadata [\#267](https://github.com/gojek/feast/pull/267) ([ches](https://github.com/ches))
- Python SDK enhancements [\#264](https://github.com/gojek/feast/pull/264) ([woop](https://github.com/woop))
- Use a symlink for Java SDK's protos [\#263](https://github.com/gojek/feast/pull/263) ([ches](https://github.com/ches))
- Clean up the Maven build [\#262](https://github.com/gojek/feast/pull/262) ([ches](https://github.com/ches))
- Add golang SDK [\#261](https://github.com/gojek/feast/pull/261) ([zhilingc](https://github.com/zhilingc))
- Move storage configuration to serving [\#254](https://github.com/gojek/feast/pull/254) ([zhilingc](https://github.com/zhilingc))
- Serving API changes for 0.3 [\#253](https://github.com/gojek/feast/pull/253) ([zhilingc](https://github.com/zhilingc))

## [v0.1.8](https://github.com/gojek/feast/tree/v0.1.8) (2019-10-30)

[Full Changelog](https://github.com/gojek/feast/compare/v0.1.2...v0.1.8)

**Implemented enhancements:**

- Feast cli config file should be settable by an env var [\#149](https://github.com/gojek/feast/issues/149)
- Helm chart for deploying feast using Flink as runner [\#64](https://github.com/gojek/feast/issues/64)
- Get ingestion metrics when running on Flink runner [\#63](https://github.com/gojek/feast/issues/63)
- Move source types into their own package and discover them using java.util.ServiceLoader [\#61](https://github.com/gojek/feast/issues/61)
- Change config to yaml [\#51](https://github.com/gojek/feast/issues/51)
- Ability to pass runner option during ingestion job submission [\#50](https://github.com/gojek/feast/issues/50)

**Fixed bugs:**

- Fix Print Method in Feast CLI [\#211](https://github.com/gojek/feast/issues/211)
- Dataflow monitoring by core is failing with incorrect job id [\#153](https://github.com/gojek/feast/issues/153)
- Feast core crashes without logger set [\#150](https://github.com/gojek/feast/issues/150)

**Merged pull requests:**

- Remove redis transaction [\#280](https://github.com/gojek/feast/pull/280) ([pradithya](https://github.com/pradithya))
- Fix tracing to continue from existing trace created by grpc client [\#245](https://github.com/gojek/feast/pull/245) ([pradithya](https://github.com/pradithya))

## [v0.1.2](https://github.com/gojek/feast/tree/v0.1.2) (2019-08-23)

[Full Changelog](https://github.com/gojek/feast/compare/v0.1.1...v0.1.2)

**Fixed bugs:**

- Batch Import, feature with datetime format issue [\#203](https://github.com/gojek/feast/issues/203)
- Serving not correctly reporting readiness check if there is no activity [\#190](https://github.com/gojek/feast/issues/190)
- Serving stop periodically reloading feature specification after a while [\#188](https://github.com/gojek/feast/issues/188)

**Merged pull requests:**

- Add `romanwozniak` to prow owners config [\#216](https://github.com/gojek/feast/pull/216) ([romanwozniak](https://github.com/romanwozniak))
- Implement filter for create dataset api [\#215](https://github.com/gojek/feast/pull/215) ([pradithya](https://github.com/pradithya))
- expand raw column to accomodate more features ingested in one go [\#213](https://github.com/gojek/feast/pull/213) ([budi](https://github.com/budi))
- update feast installation docs [\#210](https://github.com/gojek/feast/pull/210) ([budi](https://github.com/budi))
- Add Prow job for unit testing Python SDK [\#209](https://github.com/gojek/feast/pull/209) ([davidheryanto](https://github.com/davidheryanto))
- fix create\_dataset [\#208](https://github.com/gojek/feast/pull/208) ([budi](https://github.com/budi))
- Update Feast installation doc [\#207](https://github.com/gojek/feast/pull/207) ([davidheryanto](https://github.com/davidheryanto))
- Fix unit test cli in prow script not returning correct exit code [\#206](https://github.com/gojek/feast/pull/206) ([davidheryanto](https://github.com/davidheryanto))
- Fix pytests and make TS conversion conditional [\#205](https://github.com/gojek/feast/pull/205) ([zhilingc](https://github.com/zhilingc))
- Use full prow build id as dataset name during test [\#200](https://github.com/gojek/feast/pull/200) ([davidheryanto](https://github.com/davidheryanto))
- Add Feast CLI / python SDK documentation [\#199](https://github.com/gojek/feast/pull/199) ([romanwozniak](https://github.com/romanwozniak))
- Update library version to fix security vulnerabilities in dependencies [\#198](https://github.com/gojek/feast/pull/198) ([davidheryanto](https://github.com/davidheryanto))
- Update Prow configuration for Feast CI [\#197](https://github.com/gojek/feast/pull/197) ([davidheryanto](https://github.com/davidheryanto))
- \[budi\] update python sdk quickstart [\#196](https://github.com/gojek/feast/pull/196) ([budi](https://github.com/budi))
- Readiness probe [\#191](https://github.com/gojek/feast/pull/191) ([pradithya](https://github.com/pradithya))
- Fix periodic feature spec reload [\#189](https://github.com/gojek/feast/pull/189) ([pradithya](https://github.com/pradithya))
- Fixed a typo in environment variable in installation [\#187](https://github.com/gojek/feast/pull/187) ([gauravkumar37](https://github.com/gauravkumar37))
- Revert "Update Quickstart" [\#185](https://github.com/gojek/feast/pull/185) ([zhilingc](https://github.com/zhilingc))
- Update Quickstart [\#184](https://github.com/gojek/feast/pull/184) ([pradithya](https://github.com/pradithya))
- Continuous integration and deployment \(CI/CD\) update [\#183](https://github.com/gojek/feast/pull/183) ([davidheryanto](https://github.com/davidheryanto))
- Remove feature specs being able to declare their serving or warehouse stores [\#159](https://github.com/gojek/feast/pull/159) ([tims](https://github.com/tims))

## [v0.1.1](https://github.com/gojek/feast/tree/v0.1.1) (2019-04-18)

[Full Changelog](https://github.com/gojek/feast/compare/v0.1.0...v0.1.1)

**Fixed bugs:**

- Fix BigQuery query template to retrieve training data [\#182](https://github.com/gojek/feast/pull/182) ([davidheryanto](https://github.com/davidheryanto))

**Merged pull requests:**

- Add python init files [\#176](https://github.com/gojek/feast/pull/176) ([zhilingc](https://github.com/zhilingc))
- Change pypi package from Feast to feast [\#173](https://github.com/gojek/feast/pull/173) ([zhilingc](https://github.com/zhilingc))

## [v0.1.0](https://github.com/gojek/feast/tree/v0.1.0) (2019-04-09)

[Full Changelog](https://github.com/gojek/feast/compare/v0.0.2...v0.1.0)

**Implemented enhancements:**

- Removal of storing historical value of feature in serving storage [\#53](https://github.com/gojek/feast/issues/53)
- Remove feature "granularity" and relegate to metadata [\#17](https://github.com/gojek/feast/issues/17)

**Closed issues:**

- Add ability to name an import job [\#167](https://github.com/gojek/feast/issues/167)
- Ingestion retrying an invalid FeatureRow endlessly [\#163](https://github.com/gojek/feast/issues/163)
- Ability to associate data ingested in Warehouse store to its ingestion job [\#145](https://github.com/gojek/feast/issues/145)
- Missing \(Fixing\) unit test for FeatureRowKafkaIO [\#132](https://github.com/gojek/feast/issues/132)

**Merged pull requests:**

- Catch all kind of exception to avoid retrying [\#171](https://github.com/gojek/feast/pull/171) ([pradithya](https://github.com/pradithya))
- Integration test [\#170](https://github.com/gojek/feast/pull/170) ([zhilingc](https://github.com/zhilingc))
- Proto error [\#169](https://github.com/gojek/feast/pull/169) ([pradithya](https://github.com/pradithya))
- Add --name flag to submit job [\#168](https://github.com/gojek/feast/pull/168) ([pradithya](https://github.com/pradithya))
- Prevent throwing RuntimeException when invalid proto is received [\#166](https://github.com/gojek/feast/pull/166) ([pradithya](https://github.com/pradithya))
- Add davidheryanto to OWNER file [\#165](https://github.com/gojek/feast/pull/165) ([pradithya](https://github.com/pradithya))
- Check validity of event timestamp in ValidateFeatureRowDoFn [\#164](https://github.com/gojek/feast/pull/164) ([pradithya](https://github.com/pradithya))
- Remove granularity [\#162](https://github.com/gojek/feast/pull/162) ([pradithya](https://github.com/pradithya))
- Better Kafka test [\#160](https://github.com/gojek/feast/pull/160) ([tims](https://github.com/tims))
- Simplify and document CLI building steps [\#158](https://github.com/gojek/feast/pull/158) ([thirteen37](https://github.com/thirteen37))
- Fix link typo in README.md [\#156](https://github.com/gojek/feast/pull/156) ([pradithya](https://github.com/pradithya))
- Add Feast admin quickstart guide [\#155](https://github.com/gojek/feast/pull/155) ([thirteen37](https://github.com/thirteen37))
- Pass all specs to ingestion by file [\#154](https://github.com/gojek/feast/pull/154) ([tims](https://github.com/tims))
- Preload spec in serving cache [\#152](https://github.com/gojek/feast/pull/152) ([pradithya](https://github.com/pradithya))
- Add job identifier to FeatureRow  [\#147](https://github.com/gojek/feast/pull/147) ([mansiib](https://github.com/mansiib))
- Fix unit tests [\#146](https://github.com/gojek/feast/pull/146) ([mansiib](https://github.com/mansiib))
- Add thirteen37 to OWNERS [\#144](https://github.com/gojek/feast/pull/144) ([thirteen37](https://github.com/thirteen37))
- Fix import spec created from Importer.from\_csv [\#143](https://github.com/gojek/feast/pull/143) ([pradithya](https://github.com/pradithya))
- Regenerate go [\#142](https://github.com/gojek/feast/pull/142) ([zhilingc](https://github.com/zhilingc))
- Flat JSON for pubsub and text files [\#141](https://github.com/gojek/feast/pull/141) ([tims](https://github.com/tims))
- Add wait flag for jobs, fix go proto path for dataset service [\#138](https://github.com/gojek/feast/pull/138) ([zhilingc](https://github.com/zhilingc))
- Fix Python SDK importer's ability to apply features [\#135](https://github.com/gojek/feast/pull/135) ([woop](https://github.com/woop))
- Refactor stores [\#110](https://github.com/gojek/feast/pull/110) ([tims](https://github.com/tims))
- Coalesce rows [\#89](https://github.com/gojek/feast/pull/89) ([tims](https://github.com/tims))
- Remove historical feature in serving store [\#87](https://github.com/gojek/feast/pull/87) ([pradithya](https://github.com/pradithya))

## [v0.0.2](https://github.com/gojek/feast/tree/v0.0.2) (2019-03-11)

[Full Changelog](https://github.com/gojek/feast/compare/v0.0.1...v0.0.2)

**Implemented enhancements:**

- Coalesce FeatureRows for improved "latest" value consistency in serving stores [\#88](https://github.com/gojek/feast/issues/88)
- Kafka source [\#22](https://github.com/gojek/feast/issues/22)

**Closed issues:**

- Preload Feast's spec in serving cache [\#151](https://github.com/gojek/feast/issues/151)
- Feast csv data upload job [\#137](https://github.com/gojek/feast/issues/137)
- Blocking call to start feast ingestion job [\#136](https://github.com/gojek/feast/issues/136)
- Python SDK fails to apply feature when submitting job [\#134](https://github.com/gojek/feast/issues/134)
- Default dump format should be changed for Python SDK [\#133](https://github.com/gojek/feast/issues/133)
- Listing resources and finding out system state [\#131](https://github.com/gojek/feast/issues/131)
- Reorganise ingestion store classes to match architecture  [\#109](https://github.com/gojek/feast/issues/109)

## [v0.0.1](https://github.com/gojek/feast/tree/v0.0.1) (2019-02-11)

[Full Changelog](https://github.com/gojek/feast/compare/ec9def2bbb06dc759538e4424caadd70f548ea64...v0.0.1)

**Implemented enhancements:**

- Spring boot CLI logs show up as JSON [\#104](https://github.com/gojek/feast/issues/104)
- Allow for registering feature that doesn't have warehouse store [\#5](https://github.com/gojek/feast/issues/5)

**Fixed bugs:**

- Error when submitting large import spec [\#125](https://github.com/gojek/feast/issues/125)
- Ingestion is not ignoring unknown feature in streaming source [\#99](https://github.com/gojek/feast/issues/99)
- Vulnerability in dependency \(core - jackson-databind \)  [\#92](https://github.com/gojek/feast/issues/92)
- TF file for cloud build trigger broken [\#72](https://github.com/gojek/feast/issues/72)
- Job Execution Failure with NullPointerException [\#46](https://github.com/gojek/feast/issues/46)
- Runtime Dependency Error After Upgrade to Beam 2.9.0 [\#44](https://github.com/gojek/feast/issues/44)
- \[FlinkRunner\] Core should not follow remote flink runner job to completion [\#21](https://github.com/gojek/feast/issues/21)
- Go packages in protos use incorrect repo [\#16](https://github.com/gojek/feast/issues/16)

**Merged pull requests:**

- Disable test during docker image creation [\#129](https://github.com/gojek/feast/pull/129) ([pradithya](https://github.com/pradithya))
- Repackage helm chart [\#127](https://github.com/gojek/feast/pull/127) ([pradithya](https://github.com/pradithya))
- Increase the column size for storing raw import spec [\#126](https://github.com/gojek/feast/pull/126) ([pradithya](https://github.com/pradithya))
- Update Helm Charts \(Redis, Logging\) [\#123](https://github.com/gojek/feast/pull/123) ([woop](https://github.com/woop))
- Added LOG\_TYPE environmental variable [\#120](https://github.com/gojek/feast/pull/120) ([woop](https://github.com/woop))
- Fix missing Redis write [\#119](https://github.com/gojek/feast/pull/119) ([pradithya](https://github.com/pradithya))
- add logging when error on request feature [\#117](https://github.com/gojek/feast/pull/117) ([pradithya](https://github.com/pradithya))
- run yarn run build during generate-resource [\#115](https://github.com/gojek/feast/pull/115) ([pradithya](https://github.com/pradithya))
- Add loadBalancerSourceRanges option for both serving and core [\#114](https://github.com/gojek/feast/pull/114) ([zhilingc](https://github.com/zhilingc))
- Build master [\#112](https://github.com/gojek/feast/pull/112) ([pradithya](https://github.com/pradithya))
- Cleanup warning while building proto files [\#108](https://github.com/gojek/feast/pull/108) ([pradithya](https://github.com/pradithya))
- Embed ui build & packaging into core's build [\#106](https://github.com/gojek/feast/pull/106) ([pradithya](https://github.com/pradithya))
- Add build badge to README [\#103](https://github.com/gojek/feast/pull/103) ([woop](https://github.com/woop))
- Ignore features in FeatureRow if it's not requested in import spec [\#101](https://github.com/gojek/feast/pull/101) ([pradithya](https://github.com/pradithya))
- Add override for serving service static ip [\#100](https://github.com/gojek/feast/pull/100) ([zhilingc](https://github.com/zhilingc))
- Fix go test [\#97](https://github.com/gojek/feast/pull/97) ([zhilingc](https://github.com/zhilingc))
- add missing copyright headers and fix test fail due to previous merge [\#95](https://github.com/gojek/feast/pull/95) ([tims](https://github.com/tims))
- Allow submission of kafka jobs [\#94](https://github.com/gojek/feast/pull/94) ([zhilingc](https://github.com/zhilingc))
- upgrade jackson databind for security vulnerability [\#93](https://github.com/gojek/feast/pull/93) ([tims](https://github.com/tims))
- Version revert [\#91](https://github.com/gojek/feast/pull/91) ([zhilingc](https://github.com/zhilingc))
- Fix validating feature row when the associated feature spec has no warehouse store [\#90](https://github.com/gojek/feast/pull/90) ([pradithya](https://github.com/pradithya))
- Add get command [\#85](https://github.com/gojek/feast/pull/85) ([zhilingc](https://github.com/zhilingc))
- Avoid error thrown when no storage for warehouse/serving is registered [\#83](https://github.com/gojek/feast/pull/83) ([pradithya](https://github.com/pradithya))
- Fix jackson dependency issue [\#82](https://github.com/gojek/feast/pull/82) ([zhilingc](https://github.com/zhilingc))
- Allow registration of feature without warehouse store [\#80](https://github.com/gojek/feast/pull/80) ([pradithya](https://github.com/pradithya))
- Remove branch from cloud build trigger [\#79](https://github.com/gojek/feast/pull/79) ([woop](https://github.com/woop))
- move read transforms into "source" package as FeatureSources [\#74](https://github.com/gojek/feast/pull/74) ([tims](https://github.com/tims))
- Fix tag regex in tf file [\#73](https://github.com/gojek/feast/pull/73) ([zhilingc](https://github.com/zhilingc))
- Update charts [\#71](https://github.com/gojek/feast/pull/71) ([mansiib](https://github.com/mansiib))
- Deduplicate storage ids before we fetch them [\#68](https://github.com/gojek/feast/pull/68) ([tims](https://github.com/tims))
- Check the size of result against deduplicated request [\#67](https://github.com/gojek/feast/pull/67) ([pradithya](https://github.com/pradithya))
- Add ability to submit ingestion job using Flink [\#62](https://github.com/gojek/feast/pull/62) ([pradithya](https://github.com/pradithya))
- Fix vulnerabilities for webpack-dev [\#59](https://github.com/gojek/feast/pull/59) ([budi](https://github.com/budi))
- Build push [\#56](https://github.com/gojek/feast/pull/56) ([zhilingc](https://github.com/zhilingc))
- Fix github vulnerability issue with webpack [\#54](https://github.com/gojek/feast/pull/54) ([budi](https://github.com/budi))
- Only lookup storage specs that we actually need [\#52](https://github.com/gojek/feast/pull/52) ([tims](https://github.com/tims))
- Link Python SDK RFC to PR and Issue [\#49](https://github.com/gojek/feast/pull/49) ([woop](https://github.com/woop))
- Python SDK [\#47](https://github.com/gojek/feast/pull/47) ([zhilingc](https://github.com/zhilingc))
- Update com.google.httpclient to be same as Beam's dependency [\#45](https://github.com/gojek/feast/pull/45) ([pradithya](https://github.com/pradithya))
- Bump Beam SDK to 2.9.0 [\#43](https://github.com/gojek/feast/pull/43) ([pradithya](https://github.com/pradithya))
- Add fix for tests failing in docker image [\#40](https://github.com/gojek/feast/pull/40) ([zhilingc](https://github.com/zhilingc))
- Change error store to be part of configuration instead [\#39](https://github.com/gojek/feast/pull/39) ([zhilingc](https://github.com/zhilingc))
- Fix location of Prow's Tide configuration [\#35](https://github.com/gojek/feast/pull/35) ([woop](https://github.com/woop))
- Add testing folder for deploying test infrastructure and running tests [\#34](https://github.com/gojek/feast/pull/34) ([woop](https://github.com/woop))
- skeleton contributing guide [\#33](https://github.com/gojek/feast/pull/33) ([tims](https://github.com/tims))
- allow empty string to select a NoOp write transform [\#30](https://github.com/gojek/feast/pull/30) ([tims](https://github.com/tims))
- Remove packaging ingestion as separate profile \(fix \#28\) [\#29](https://github.com/gojek/feast/pull/29) ([pradithya](https://github.com/pradithya))
- Change gopath to point to gojek repo [\#26](https://github.com/gojek/feast/pull/26) ([zhilingc](https://github.com/zhilingc))
- Fixes \#31 - errors during kafka deserializer \(passing\) test execution [\#25](https://github.com/gojek/feast/pull/25) ([baskaranz](https://github.com/baskaranz))
- Kafka IO fixes [\#23](https://github.com/gojek/feast/pull/23) ([tims](https://github.com/tims))
- KafkaIO implementation for feast [\#19](https://github.com/gojek/feast/pull/19) ([baskaranz](https://github.com/baskaranz))
- Return same type string for warehouse and serving NoOp stores [\#18](https://github.com/gojek/feast/pull/18) ([tims](https://github.com/tims))
- \#12: prefetch specs and validate on job expansion [\#15](https://github.com/gojek/feast/pull/15) ([tims](https://github.com/tims))
- Added RFC for Feast Python SDK [\#14](https://github.com/gojek/feast/pull/14) ([woop](https://github.com/woop))
- Add more validation in feature spec registration [\#11](https://github.com/gojek/feast/pull/11) ([pradithya](https://github.com/pradithya))
- Added rfcs/ folder with readme and template [\#10](https://github.com/gojek/feast/pull/10) ([woop](https://github.com/woop))
- Expose ui service rpc [\#9](https://github.com/gojek/feast/pull/9) ([pradithya](https://github.com/pradithya))
- Add Feast overview to README [\#8](https://github.com/gojek/feast/pull/8) ([woop](https://github.com/woop))
- Directory structure changes [\#7](https://github.com/gojek/feast/pull/7) ([zhilingc](https://github.com/zhilingc))
- Change register to apply [\#4](https://github.com/gojek/feast/pull/4) ([zhilingc](https://github.com/zhilingc))
- Empty response handling in serving api [\#3](https://github.com/gojek/feast/pull/3) ([pradithya](https://github.com/pradithya))
- Proto file fixes [\#1](https://github.com/gojek/feast/pull/1) ([pradithya](https://github.com/pradithya))
