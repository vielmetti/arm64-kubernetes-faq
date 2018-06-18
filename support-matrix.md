## Kubernetes supported ARM device matrix

This is an (incomplete) list of ARM devices that have been tested or are in the midst of being tested against various versions of Kubernetes and its accompanying components.

| device | OS/kernel | Docker verion | Kubernetes master version | Kubernetes worker version |
|-|-|-|-|-|
| Rock64 | [Xenial minimal rock64 0.5.15/4.4](https://github.com/ayufan-rock64/linux-build/releases/tag/0.5.15)  | docker-ce=18.04.0~ce~3-0~ubuntu | 1.9.7, 1.10.2 | 1.9.7, 1.10.2 |
| Raspberry Pi 3B+ | [Raspbian Strectch Lite/4.14](https://www.raspberrypi.org/downloads/raspbian/) | docker-ce=18.04.0~ce~3-0~raspbian | 1.9.7, 1.10.2 | 1.9.7, 1.10.2 |
| Cavium ThunderX (Packet c1.large.arm) | Debian 9 | | | |

## Kubernetes software matrix

This is a running list of either officially supported ARM ports or those done by member of the community.

| Service | Version | Kubernetes tested version | Officially supported | Device(s) tested on |
|-|-|-|-|-|
| Weave | 2.3.0 | 1.10.2 | yes | RPi, Rock64 |
| Flannel| | | yes |
| MetalLB | v0.4.5+ | 1.10.2 | yes | Rock64 |
| Etcd | 3.1.12| 1.10.2 | yes | RPi |
| CoreDNS | 1.0.6+ | 1.10.2 | yes | RPi |
| Kube-DNS | 1.14.8 | 1.10.2 | yes | RPi |
| Nginx Ingress controller | 0.16.0 | | yes |
| Traefik | | | yes |
| Heapster (deprecated) | 1.5.0 | 1.10.2 | yes | Rock64 |
| * Metrics server | 0.2.1 | 1.10.2 | yes | Rock64 |
| Kubernetes Dashboard | 1.8.3 | 1.10.2 | yes | Rock64 |
| Prometheus | 2.1.1 | 1.10.2 | [no](https://github.com/carlosedp/prometheus-ARM) | Rock64 |
| Prometheus Operator | 0.17.0| 1.10.2 | [no](https://github.com/carlosedp/prometheus-operator-ARM) | |
| Helm Tiller | v2.9.1 | 1.10.2 | [no](https://github.com/jessestuart/tiller-multiarch) | Rock64 |

NOTE: Asterisks indicate that there have been some problems getting the service to work.  Either due to a bug or some other limitation.

## Known issues

There are some open issues currently that are causing issues for folks trying to deploy ARM clusters.

* [kubeadm init stuck - 1.10.3](https://github.com/kubernetes/kubernetes/issues/61277#issuecomment-390484103)
* [etcd doesn'r run on arm64](https://github.com/coreos/etcd/issues/5054)
* [Nginx Ingress controller crash on boot](https://github.com/kubernetes/ingress-nginx/issues/2547) (merged - should be released in 0.16.0)
* [cert-manager port to arm64](https://github.com/jetstack/cert-manager/pull/614)

Please feel free to open a PR with any other devices or software that has been tested or otherwise proven to be stable, or if there are blocking issues feel free to add them to the list.
