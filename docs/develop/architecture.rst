Architecture
============

This page will give you a generic overview on Systers Portal project architecture.
As any other Django project Portal organizes its functionality in several apps:

* **blog** - handles showing, adding, editing and deleting news and resources.
* **common** - generic functionality that can't be part of any other app.
  For example, landing, about, contact pages, generic models, helpers, mixins
  that are used in several apps.
* **community** - community and subcommunities functionality, like
  adding new communities, views and editing community profiles, showing, adding,
  editing and deleting community pages, managing permissions regarding each
  community.
* **membership** - handles showing, creating, approving and rejecting join
  requests to a community, removing and inviting users to become members of a
  community.
* **users** - showing and editing user personal profile.
* **meetup** - handles meetup locations and meetup functionality.

The templates are placed inside ``systers_portal/templates`` folder organized
in a folder structure similar to the apps tree. Respectively the templates
location matches the views location.

Each app along with models, views, urls and other app related code (admin, forms,
mixins, utils) contains a folder with migrations and tests. The migrations
are generated by Django and shouldn't be edited manually. The tests folder
mimics the app modules covering each module with a separate test file. For
example, tests for ``app_name/models.py`` are contained in the
``app_name/tests/test_models.py``.
