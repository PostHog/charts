# Posthog Charts

This repository contains helm charts for PostHog:

* [PostHog](https://github.com/PostHog/charts/blob/master/charts/posthog/README.md)

```shell script
helm repo add posthog https://posthog.github.io/charts/
helm repo update
helm install posthog posthog/posthog
```

**NOTE - If Helm hangs while installing this chart try increasing the memory of your nodes**

As a baseline we suggest having at least 4gb of memory per node


## GitHub Actions

We have an action to create new releases automatically. On pushes to `master`, it checks that the version was bumped and then:

- Creates a GitHub release from the tag
- Pushes a new release to https://posthog.github.io/charts/

If the bot fails to create a release, take a look at the [upstream action repo](https://github.com/helm/chart-releaser-action) to see if there were any breaking changes.