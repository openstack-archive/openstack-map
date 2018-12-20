=======================
 Using This Repository
=======================

This repository contains information about OpenStack first-order
deliverables, to be used to generate the OpenStack map and "software"
pages on the openstack.org website.

What should be included
=======================

The goal is to provide a user-facing view of OpenStack deliverables.
As such, only first-order deliverables (components that users actually
opt into installing) are presented. Libraries, pure dependencies and
other second-level deliverables should not be included.

File structure
==============

This repository contains one file for the OpenStack components themselves
(openstack_components.yaml), one for tools that can be used to deploy
them (deployment_tools.yaml) and one for tools that can be used client-side
to interact with them (sdks.yaml).

Each file has a super-structure with tabs and categories, under which each
component can be added.

Component schema
================

Each component is defined by a YAML dictionary with the following keys:

``name``
  The component name (mandatory).

``title``
  A user-friendly short description of the component role (mandatory).

``docs-title``
  Text to use for a link to further documentation (optional).

``docs-url``
  URL to use for a link to further documentation (optional).

``desc``
  Long description of the component role (mandatory).

``project-team``
  Name of the project team that produces this deliverable, as found in
  the openstack/governance repository in the reference/projects.yaml file
  (mandatory).

``support-teams``
  *List* of other project teams (such as I18n, Docs...) to credit for helping
  in the production of that component, as found in the openstack/governance
  repository in the reference/projects.yaml file (optional).

``since``
  First OpenStack release that included that component (optional).

``video``
  Video to embed. Currently only supports linking to YouTube videos (optional).

  ``id``
    YouTube ID for the video.

  ``title``
    Title for the video.

  ``desc``
    Description of the video.

``dependencies``
  *List* of other component names that are hard dependencies for this component
  (can't work without them) (optional, only for openstack_components.yaml).

``see-also``
  *List* of other component names that are soft dependencies for this component
  (benefits of the presence of them) (optional, only for
  openstack_components.yaml).
