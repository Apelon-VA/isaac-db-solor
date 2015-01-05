ISAAC-DB-SOLOR
==============

A project for creating official ISAAC SOLOR Database releases with the desired dataset (including various transforms)

To just build the DB:

`mvn clean compile`

This will create the DB in the project-specific sub-folder {build-config}/target/[descriptive-name].bdb

To create the DB, and also create a zip package of the DB, run:
	
`mvn clean package`

When you are happy with the resulting database - to publish it to an archiva server assemble a command along the lines of:

`mvn clean deploy -DaltDeploymentRepository=maestro::default::https://va.maestrodev.com/archiva/repository/data-files/`

Assuming that doesn't fail - tag the code that published the build:

`jgitflow:release-start jgitflow:release-finish`