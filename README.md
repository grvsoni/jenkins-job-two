# jenkins-job-two

Pipeline job that deploys **orders-api** to **staging**.

- [`Jenkinsfile`](Jenkinsfile) — reads `config.json` and passes its values into `runConfigJob(serviceName: ..., environment: ...)`.
- [`config.json`](config.json) — parameters consumed by the shared step:
  ```json
  { "serviceName": "orders-api", "environment": "staging" }
  ```
- [`config.xml`](config.xml) — importable Jenkins pipeline-job definition.

The logic lives entirely in the shared library
(`grvsoni/jenkins-shared-library`); this repo only supplies the config values.
# jenkins-job-two
