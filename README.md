# Alexander Jelinek

Platform Engineer. I keep infrastructure out of the way of people who have
better things to think about.

Most of my colleagues are software engineers working on domain problems. They
shouldn't need to know what a CNI is to ship a feature. So I build the layer in
between: self-service where possible, guardrails where necessary, and as few
tickets as I can manage in either direction.

## What that looks like in practice

Running an in-house Kubernetes platform end to end — the cluster itself, plus
the parts everyone notices the moment they break: ingress controllers,
external-dns, Calico. Helping teams get their CI/CD talking to Kubernetes
without each of them inventing a personal deployment story.

Underneath it, an OpenStack installation I helped build and run, with Kubespray
assembling the clusters on top. Operating both layers yourself removes the
comfort of blaming the other one.

Automating namespace provisioning until "I need an environment" stopped being a
ticket. Not just the namespace: the quotas, annotations and defaults that make
it actually usable on arrival.

Then leading the technical side of moving that platform onto Google Kubernetes
Engine. Migrations are where you find out which of your abstractions were real.

Lately I've been helping build an in-house agentic harness. Familiar
infrastructure, unfamiliar failure modes.

## Upstream

Some of that work went back where it came from. I contribute to
[kubespray](https://github.com/kubernetes-sigs/kubespray), mostly around the
seams — Cinder CSI options, cloud-controller-manager DNS behaviour, storage
class defaults, secret encryption at rest, container runtime checksums.
Unglamorous, load-bearing things that are only interesting to whoever is on call.

## An opinion I'll defend

I like Kubernetes. I've worked with it long enough to have run it the hard way,
on-prem, before handing it to a managed service — and I still like it.

Which is exactly why I'll tell you when your team doesn't need it. Plenty of
workloads are better served by something boring, and the best platform decision
is sometimes the one that removes a platform.

## Things I've built

**[tenama](https://github.com/Payback159/tenama)** — a REST API for temporary
namespaces in shared clusters. Creation, lifetime, cleanup. Born from watching
developers wait on a cluster admin for something that should take ten seconds.

**[OpenFero](https://github.com/OpenFero/openfero)** — event-triggered job
scheduler for recovery tasks. Alerts that always ended in the same three
commands should probably just run those three commands.

**[namespace-resizer](https://github.com/Payback159/namespace-resizer)** —
resource quotas that adjust without a human in the loop.

**[enshrouded-operator](https://github.com/Payback159/enshrouded-operator)** — a
game server I already ran for my friends, rebuilt as a proper operator. I wanted
to understand the operator pattern rather than read about it, and reconciling
something I actually cared about beat reconciling a tutorial.

**[sample-oidc-app](https://github.com/Payback159/sample-oidc-app)** — a
deliberately tiny app whose only job is to make the OIDC flow visible. Not for
production. For the moment it finally clicks.

And occasionally something with no infrastructure in it at all:
[notenschluessel](https://github.com/Payback159/notenschluessel), a grading-scale
tool for teachers, because that particular spreadsheet had it coming.

## Elsewhere

[jelinek.website](https://jelinek.website/) ·
[LinkedIn](https://www.linkedin.com/in/alexanderjelinek/)

---

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Payback159/Payback159/output/github-contribution-grid-snake-dark.svg">
  <img alt="A snake eating my contribution graph" src="https://raw.githubusercontent.com/Payback159/Payback159/output/github-contribution-grid-snake.svg">
</picture>
