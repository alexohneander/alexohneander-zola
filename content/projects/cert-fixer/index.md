+++
title = "cert-fixer"
description = "Watch k8s Resources to fix self propagation check for clusters behind NAT."
weight = 30

[taxonomies]
tags = ["Rust", "Kubernetes", "CoreDNS", "BareMetal" ]

[extra]
local_image = "projects/cert-fixer/zutsu_logo.webp"
social_media_card = "social_cards/projects_doteki.jpg"
canonical_url = "https://alexohneander.de/projects/rustysearch/"
add_src_to_code_block = true
+++

### Why does this project exist?

If you run a Kubernetes cluster behind a NAT and want to create certificates with the **Cert-Manager**, you quickly run into the problem that the Self Propagation check fails. This issue can be fixed with a simple line of code in the **CoreDNS** config. But now you don't want to adjust the **CoreDNS** Config for every Ingress and restart the Pod afterwards. The **cert-fixer** is supposed to be a quick remedy for this.

### How does it work?

The **cert-fixer** is a simple **Kubernetes** Pod that checks continuously if some Ingresses have been created or deleted. If this is the case, the **CoreDNS** ConfigMap should be updated and the **CoreDNS** Pod should be restarted.

### How to use it?

```bash
kubectl apply -f https://raw.githubusercontent.com/alexohneander/cert-fixer/main/deployment/deployment.yaml
```

### How to configure it?

The **cert-fixer** is configured via environment variables. The following variables are available:

| Variable | Description | Default |
| --- | --- | --- |
| INGRESS_SERVICE | The name of the Ingress Controller Service | ingress-nginx-controller.ingress-nginx.svc.cluster.local |
