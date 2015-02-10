ISAAC-DB-SOLOR
==============

A project for creating official ISAAC SOLOR Database releases with the desired dataset (including various transforms)

To just build the DB:

`mvn clean compile`

This will create the DB in target/[descriptive-name].bdb

To create the DB, and also create a zip package of the DB, run:
	
`mvn clean package`

When you are happy with the resulting database - to publish it to an archiva server and properly tag and version it, assemble a command along the lines of:

`mvn jgitflow:release-start jgitflow:release-finish -DreleaseVersion=Baseline_0x -DdevelopmentVersion=Baseline_0y-SNAPSHOT -DaltDeploymentRepository=maestro::default::https://va.maestrodev.com/archiva/repository/va-releases/`