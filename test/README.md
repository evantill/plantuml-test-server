# HOWTO test receiving a release event using act

- Install [nektos/act](https://github.com/nektos/act)
- Create a `.secrets` file with the github PAT Token
  ```
  GITHUB_TOKEN=ghp_...
  ```
- Run `act -l` to list workflows
- Run `act` to simulate the receive event :
  ```shell
  act --job "update-maven-pom" -e test/repository_dispatch_on_release_evt.json
  ```
