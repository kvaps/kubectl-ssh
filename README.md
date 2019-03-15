# kubectl-ssh

Tiny plugin for connecting to node in the cluster over SSH.

## Features

* Getting IP-address of the node from the API.
* Setting username and ssh options per context.

## Installation

```bash
curl -LO https://github.com/kvaps/kubectl-ssh/raw/master/kubectl-ssh
chmod +x ./kubectl-ssh
sudo mv ./kubectl-ssh /usr/local/bin/kubectl-ssh
```

## Usage

```bash
kubectl ssh <node>
```

## Configuration

```bash
# Set username
echo 'USERNAME=user' >> ~/.kube/ssh-config

# Set options
echo 'SSH_OPTIONS="-o LogLevel=ERROR -o StrictHostKeyChecking=no -o UserKnownHostsFile=/dev/null"' >> ~/.kube/ssh-config

# Set username for specific context
echo 'STAGE_USERNAME=user' >> ~/.kube/ssh-config

# Set options for specific context
echo 'STAGE_SSH_OPTIONS="-o LogLevel=ERROR -o StrictHostKeyChecking=no -o UserKnownHostsFile=/dev/null"' >> ~/.kube/ssh-config
```
