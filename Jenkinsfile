// Load the shared library named 'shared-lib' (configured under
// Manage Jenkins -> Global Pipeline Libraries).
@Library('shared-lib') _

node {
    checkout scm

    // Read the params from this repo's config.json ...
    def config = readJSON file: 'config.json'

    // ... and pass them explicitly into the shared-library function.
    runConfigJob(serviceName: config.serviceName, environment: config.environment)
}
