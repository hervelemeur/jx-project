## project spring

Create a new Spring Boot application and import the generated code into Git and Jenkins for CI/CD

### Usage

```
project spring
```

### Synopsis

Creates a new Spring Boot application and then optionally setups CI/CD pipelines and GitOps promotion.
  
      You can see a demo of this command here: [https://jenkins-x.io/demos/create_spring/](https://jenkins-x.io/demos/create_spring/)
  
      For more documentation see: [https://jenkins-x.io/developing/create-spring/](https://jenkins-x.io/developing/create-spring/)
  
See Also: 

  * jx create project : https://jenkins-x.io/commands/jx_create_project

### Examples

  # Create a Spring Boot application where you use the terminal to pick the values
  jx project spring
  
  # Creates a Spring Boot application passing in the required dependencies
  jx project spring -d web -d actuator
  
  # To pick the advanced options (such as what package type maven-project/gradle-project) etc then use
  jx project spring -x
  
  # To create a gradle project use:
  jx project spring --type gradle-project

### Options

```
  -x, --advanced                       Advanced mode can show more detailed forms for some resource kinds like springboot
  -a, --artifact string                Artifact ID to generate
  -b, --batch-mode                     Runs in batch mode without prompting for user input
  -t, --boot-version string            Spring Boot version
      --branches string                The branch pattern for branches to trigger CI/CD pipelines on
      --canary                         should we use canary rollouts (progressive delivery) by default for this application. e.g. using a Canary deployment via flagger. Requires the installation of flagger and istio/gloo in your cluster
      --credentials string             The Jenkins credentials name used by the job
  -d, --dep stringArray                Spring Boot dependencies
      --deploy-kind string             The kind of deployment to use for the project. Should be one of knative, default
      --disable-updatebot              disable updatebot-maven-plugin from attempting to fix/update the maven pom.xml
      --docker-registry-org string     The name of the docker registry organisation to use. If not specified then the Git provider organisation will be used
      --dry-run                        Performs local changes to the repo but skips the import into Jenkins X
      --git-kind string                the kind of git server to connect to
      --git-provider-url string        Deprecated: please use --git-server
      --git-server string              the git server URL to create the scm client
      --git-token string               the git token used to operate on the git repository. If not specified it's loaded from the git credentials file
      --git-user string                the git username used to operate on the git repository
  -g, --group string                   Group ID to generate
  -h, --help                           help for spring
      --hpa                            should we enable the Horizontal Pod Autoscaler for this application.
      --import-commit-message string   Specifies the initial commit message used when importing the project
  -m, --import-mode string             The import mode to use. Should be one of Jenkinsfile, YAML
  -j, --java-version string            Java version
      --jenkinsfile string             The name of the Jenkinsfile to use. If not specified then 'Jenkinsfile' will be used
      --jenkinsfilerunner string       if you want to import into Jenkins X with Jenkinsfilerunner this argument lets you specify the container image to use
      --jx                             if you want to default to importing this project into Jenkins X instead of a Jenkins server if you have a mixed Jenkins X and Jenkins cluster
  -k, --kind stringArray               Default dependency kinds to choose from (default [Core,Web,Template Engines,SQL,I/O,Ops,Spring Cloud GCP,Azure,Cloud Contract,Cloud AWS,Cloud Messaging,Cloud Tracing])
  -l, --language string                Language to generate
      --name string                    Specify the Git repository name to import the project into (if it is not already in one)
      --no-dev-pr                      disables generating a Pull Request on the development git repository
      --no-import                      Disable import after the creation
      --no-pack                        Disable trying to default a Dockerfile and Helm Chart from the build pack
      --no-start                       disables starting a release pipeline when imprting/creating a new project
      --org string                     Specify the Git provider organisation to import the project into (if it is not already in one)
  -o, --output-dir string              Directory to output the project to. Defaults to the current directory
      --pack string                    The name of the build pack to use. If none is specified it will be chosen based on matching the source code languages
  -p, --packaging string               Packaging
      --pr-poll-period duration        the time between polls of the Pull Request on the development environment git repository (default 20s)
      --pr-poll-timeout duration       the maximum amount of time we wait for the Pull Request on the development environment git repository (default 20m0s)
      --scheduler string               The name of the Scheduler configuration to use for ChatOps when using Prow
      --service-account string         The Kubernetes ServiceAccount to use to run the initial pipeline (default "tekton-bot")
      --type string                    Project Type (such as maven-project or gradle-project)
      --use-default-git                use default git account
      --wait-for-pr                    waits for the Pull Request generated on the development envirionment git repository to merge (default true)
```

### SEE ALSO

* [project](project.md)	 - Create a new project by importing code, creating a quickstart or custom wizard for spring

###### Auto generated by spf13/cobra on 5-Oct-2020
