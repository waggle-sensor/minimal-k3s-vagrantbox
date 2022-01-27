# Minimal k3s Vagrantbox

This repo provides a Vagrantfile for getting started with a minimal, vanilla [k3s](https://k3s.io) installation in a box.

## Usage

Make sure [Vagrant](https://www.vagrantup.com) is installed and you are working in this repo's base directory.

First, we'll spin up the box by running:

```sh
vagrant up
```

Once the box is running, we'll ssh in and become root.

```sh
vagrant ssh
sudo -s
```

Let's confirm that we can talk to Kubernetes by running:

```sh
kubectl get all
```

You should see something like:

```text
NAME                 TYPE        CLUSTER-IP   EXTERNAL-IP   PORT(S)   AGE
service/kubernetes   ClusterIP   10.43.0.1    <none>        443/TCP   4m53s
```

Great! It will take a moment for all the system containers to finish pulling and run, but
otherwise, you are ready to start experimenting!

When you are done, you can destroy the environment by running:

```sh
vagrant destroy
```
