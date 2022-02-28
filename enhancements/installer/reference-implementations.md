---
title: reference-implementations
authors:
  - "@jufaerma"
  - "#team-splat"
# reviewers:
#   - TBD
# approvers:
#   - TBD
# api-approvers: # in case of new or modified APIs or API extensions (CRDs, aggregated apiservers, webhooks, finalizers)
#   - TBD
creation-date: 2022-02-28
last-updated: 2022-02-28
# tracking-link: # link to the tracking ticket (for example: Jira Feature or Epic ticket) that corresponds to this enhancement
#   - TBD
# see-also:
#   - "/enhancements/this-other-neat-thing.md"
# replaces:
#   - "/enhancements/that-less-than-great-idea.md"
# superseded-by:
#   - "/enhancements/our-past-effort.md"
---

# Reference Implementations

This enchancement adds reference implementations (RIs) for openshift providers, so that technical expectations are clearly communicated and a guideline for development is offered to partners and to the community. The reference implementations are guided by the implementation of recent providers and the current features of the openshift platform.

## Provider Stories

The reference implementations are built from the perspective of the provider, referenced generally as "Reference Cloud" in this enhancement. The more frequent a business case, the more valuable is the reference implementation.

### Installer Provisioning
Enables `openshift-install` to create and destroy a cluster on Reference Cloud, which is provisioned, observed and tested automatically.

### Application Delivery
Enables delivery of applications directly from source repository to Reference Cloud, using continuous integration and delivery pipelines.

## Implementation Details/Notes/Constraints 

### Low-coupling

The implementation of provider features should depend as little as posible on openshift repositories and artifacts. The lower the coubpling between providers and openshift code, the more both can evolve independently. As more reference implementations are provided, we'll be able to map and reduce the coupling points.

### Gradual Evolution

Let partners evolve in architectre and features as adequate to the business context. The reference implementations should map to a layered maturity model so that expectations are clearly set at each stage.

## Design Details

### Open Questions

What is the list of artifacts to be built initially?

### Test Plan

Apply the openshift / kubernetes compliance testing to the reference implementation.
