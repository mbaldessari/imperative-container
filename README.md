# Imperative Container

imperative container for simplified execution of imperative commands in each of the patterns.


## Installed Software

|          name    |  type    |version|
|:----------------:|:--------:|:-----:|
|ansible           |pip       |2.16.11|
|ansible.posix     |collection|1.6.0  |
|ansible-runner    |pip       |2.4.0  |
|ansible.utils     |collection|5.1.1  |
|community.general |collection|9.4.0  |
|community.okd     |collection|4.0.0  |
|git-core          |package   |2.43.5 |
|jmespath          |pip       |1.0.1  |
|jq                |package   |1.6    |
|kubernetes.core   |collection|5.0.0  |
|kubernetes        |pip       |31.0.0 |
|make              |package   |4.3    |
|openshift         |binary    |4.16.14|
|python3-pip       |package   |21.2.3 |
|python            |package   |3.11.7 |
|rhvp.cluster_utils|collection|1.0.1  |
|sshpass           |package   |1.09   |

## Usage
**Pull the image**
```bash
podman pull quay.io/hybridcloudpatterns/imperative-container:latest
```

**Use image to execute a playbook**
```bash
podman run -it --rm --net=host quay.io/hybridcloudpatterns/imperative-container:latest ansible-playbook <playbook>.yml
```

## Build the image
Just run: `make build` and both amd64 and arm64 will be built locally (you will need the qemu-user-static package installed)

To upload the image to the official repository, run: `make UPLOADREGISTRY=quay.io/hybridcloudpatterns upload` (by default it uploads somewhere else
to try and avoid accidental uploads)

