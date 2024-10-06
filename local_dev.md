## True Anthem Local Development Setup

### Terminal shell recommendation

I recommend TA team's favorite terminal [Warp](https://www.warp.dev/).

My personal shell recommendation is `ohmyzsh`. Install using the following command

```shell
$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

then following instructions to setup your own terminal.

You can customize your own theme by following this [guide](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes).

### Install Homebrew for "managing stuff" on your Mac

```shell
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Code editor recommedations

- Anything Jetbrains or
- VSCode (fuck this) or
- Vim (kill yourself)

### Install Golang dependencies

Install Go:

```shell
$ brew install go
```

Install Go linter:

```shell
$ brew install staticcheck
```

Install Go security checker:

```shell
$ brew install gosec
```

Install GRPC Go code generator:

```shell
$ brew install protoc-gen-go-grpc
```

### Install JS dependencies

Install NVM (Node Version Manager)

```shell
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash
```

Install Node and npm (v20 is latest stable)

```shell
$ nvm install v20
```

Install Yarn (better npm)

```shell
$ npm install --global yarn
```

### Install Gcloud dependencies

Install `gcloud-cli` at https://cloud.google.com/sdk/docs/install.

Authenticate `gcloud-cli`:

```shell
$ gcloud auth application-default login
```

### Install Docker/Kubernetes dependencies

#### Install Docker

Download Docker Desktop at https://docs.docker.com/desktop/install/mac-install/.

Configure TA container registry:
```$
gcloud auth configure-docker us-east1-docker.pkg.dev
```

#### Install `kubectl` for interacting with Kubernetes:

```shell
$ brew install kubectl
```

#### Install `kustomize` for configuration management:

```shell
$ brew install kustomize
```

### Setup Github repository

Connect to Github with SSH by following these guides:

- [Generating a new SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
- [Adding a new SSH key to your Github account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
- [Testing your SSH connection](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/testing-your-ssh-connection)

Clone the `colossus` repository (Contact Jon to gain access to the repository):

```shell
$ git clone git@github.com:trueanthem/colossus.git
```

### Setup local configurations

#### Create Go apps configuration

Create a new folder `.nab` from `$ROOT`:

```shell
$ mkdir ~/.nab
```

In this new folder, create a new YAML configuration file:

```shell
$ touch ~/.nab/config.yaml
```

#### Create the Dashboard app configuration

Create a new folder `.dashboard` from `$ROOT`:

```shell
$ mkdir ~/.dashboard
```

In this new folder, create a new JSON configuration file:

```shell
$ touch ~/.dashboard/dashboard.json
```

Contact anyone from the Engineering team for a working configuration file.

### Launch apps:

Follow Go apps instruction at: https://github.com/trueanthem/colossus/blob/main/go/README.md.

Follow the Dashboard app instruction at: https://github.com/trueanthem/colossus/blob/main/js/dashboard/README.md.

