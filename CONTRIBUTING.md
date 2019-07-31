# Contributing

Issues, whether bugs, tasks, or feature requests are essential for keeping goldilocks great. We believe it should be as easy as possible to contribute changes that get things working in your environment. There are a few guidelines that we need contributors to follow so that we can keep on top of things.

## Code of Conduct

This project adheres to a [code of conduct](CODE_OF_CONDUCT.md). Please review this document before contributing to this project.

## Sign the CLA
Before you can contribute, you will need to sign the [Contributor License Agreement](https://cla-assistant.io/fairwindsops/goldilocks).

## Project Structure

Goldilocks can run in 3 modes.  There is a CLI that allows the manipulation of VPA objects, a dashboard, and a controller that runs in-cluster and manages VPA objects based on namespace labels. The CLI uses the cobra package and the commands are in the `cmd` folder.

## Getting Started

We label issues with the ["good first issue" tag](https://github.com/FairwindsOps/goldilocks/labels/good%20first%20issue) if we believe they'll be a good starting point for new contributors. If you're interested in working on an issue, please start a conversation on that issue, and we can help answer any questions as they come up.

## Setting Up Your Development Environment
### Prerequisites
* A properly configured Golang environment with Go 1.11 or higher
* If you want to see the local changes you make on a dashboard, you will need access to a Kubernetes cluster defined in `~/.kube/config` or the KUBECONFIG variable.
* The [vertical pod autoscaler](https://github.com/kubernetes/autoscaler/tree/master/vertical-pod-autoscaler) will need to be installed in the cluster.

### Installation
* Install the project with `go get github.com/fairwindsops/goldilocks`
* Change into the goldilocks directory which is installed at `$GOPATH/src/github.com/fairwindsops/goldilocks`
* Use `make tidy` or `make build` to ensure all dependencies are downloaded.
* See the dashboard with `go run main.go dashboard`, then open http://localhost:8080/.  This assumes that you have a working KUBECONFIG in place with access to a cluster.

## Creating a New Issue

If you've encountered an issue that is not already reported, please create an issue that contains the following:

- Clear description of the issue
- Steps to reproduce it
- Appropriate labels

## Creating a Pull Request

Each new pull request should:

- Reference any related issues
- Add tests that show the issues have been solved
- Pass existing tests and linting
- Contain a clear indication of if they're ready for review or a work in progress
- Be up to date and/or rebased on the master branch

## Creating a new release

Push a new annotated tag.  This tag should contain a changelog of pertinent changes.