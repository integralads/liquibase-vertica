liquibase-vertica
=================

#Why this repo?

This is an IAS built version of the liquibase-vertica artifact : forked from https://github.com/liquibase/liquibase-vertica.

The artifact that is being pulled down from Maven Central is not working will against the analytics-vertica-db database project: https://github.com/integralads/analytics-vertica-db 

It results in the error:

```
[ERROR] Failed to execute goal org.liquibase:liquibase-maven-plugin:3.4.1:update (default) on project analytics-vertica-db: Execution default of goal org.liquibase:liquibase-maven-plugin:3.4.1:update failed: An API incompatibility was encountered while executing org.liquibase:liquibase-maven-plugin:3.4.1:update: java.lang.NoSuchMethodError: liquibase.snapshot.JdbcDatabaseSnapshot$CachingDatabaseMetaData.getTables(Ljava/lang/String;Ljava/lang/String;Ljava/lang/String;[Ljava/lang/String;)Ljava/util/List;
[ERROR] -----------------------------------------------------
[ERROR] realm =    plugin>org.liquibase:liquibase-maven-plugin:3.4.1
[ERROR] strategy = org.codehaus.plexus.classworlds.strategy.SelfFirstStrategy
[ERROR] urls[0] = file:/Users/jprabhakara/.m2/repository/org/liquibase/liquibase-maven-plugin/3.4.1/liquibase-maven-plugin-3.4.1.jar
[ERROR] urls[1] = file:/Users/jprabhakara/.m2/repository/org/liquibase/ext/liquibase-verticaDatabase/1.2-1/liquibase-verticaDatabase-1.2-1.jar
[ERROR] urls[2] = file:/Users/jprabhakara/.m2/repository/com/vertica/vertica-jdbc/9.1.1/vertica-jdbc-9.1.1.jar
[ERROR] urls[3] = file:/Users/jprabhakara/.m2/repository/org/liquibase/ext/liquibase-nochangeloglock/1.1/liquibase-nochangeloglock-1.1.jar
[ERROR] urls[4] = file:/Users/jprabhakara/.m2/repository/org/codehaus/plexus/plexus-utils/1.0.4/plexus-utils-1.0.4.jar
[ERROR] urls[5] = file:/Users/jprabhakara/.m2/repository/org/liquibase/liquibase-core/3.4.1/liquibase-core-3.4.1.jar
[ERROR] Number of foreign imports: 1
[ERROR] import: Entry[import  from realm ClassRealm[maven.api, parent: null]]
[ERROR] 
[ERROR] -----------------------------------------------------
```
If a future version of org.liquibase.ext:liquibase-verticaDatabase fixes this error - we can update https://github.com/integralads/analytics-vertica-db to point to that version and decommision this repo.


###Please be mindful 

  - THIS IS A PUBLIC FORK (there is no way to make a public fork be private in the integralads org)
  - Do not check-in any IAS sensitive / keys / secrets / proprietary information in this repo 

Liquibase extension to add improved HP Vertica support

