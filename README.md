Biblio
======================

This module reproduces some, but not all, of the functionality of the
Drupal Biblio module. It defines:
- A content type called Bibliographic Reference (short name "biblio_pub"), with
  fields to store bibliographic data.
- A views page that shows all of your bibliographic data at URL /biblio within
  your site. It is sorted in alphabetic order by author (choosing the earliest
  author in alphabetic order for each entry).
- A layout that overrides the default for the taxonomy page, so that if you
  visit the taxonomy page for an author, it shows the bibliographic records for
  that author. If you have customized the default layout on your site, you will
  most likely want to customize this taxonomy page layout in the same way.
- A Feeds configuration for importing bibliographic information in MODS format
  into Bibliographic Reference content items. If you have the required Feeds
  modules installed (see below), you can go to /import in your site and import
  MODS data. (See http://www.loc.gov/standards/mods/ for more on the Library of
  Congress MODS format for bibliographic data.) The feeds configuration could be
  edited to take data from a URL instead of a local file.

### Submodules

Some of the biblio submodules have not been ported yet.

If you are using unported submodules and would like to see them available for
use in Backdrop, please let us know which you are using on this issue:
https://github.com/backdrop-contrib/biblio/issues/10


Requirements
------------

This module requires the following contributed modules:
- Multifield (machine name: multifield)
- Field Group (field_group)

To import bibliographic information from external soures, you will also need:
- Feeds (feeds) -- a release after 1.x-1.0.0-beta
- Feeds XPath Parser (feeds_xpathparser)
- Job Scheduler (job_scheduler) -- required by Feeds, but not used directly


Version Numbers and Upgrading from Drupal 7
--------------------------------------------

All recommended releases of the Drupal 7 module are on the 1.x branch.

To upgrade to Backdrop: Make sure your Drupal 7 site is are on the latest
1.x release (that is version 7.x-1.6 as of Feb 2024).

The Backdrop module is on a 2.x branch because there were some sigificant
chanes to the underlying structure of a bibliographic reference. It is now a
node so that it can benefit from all the other features of modern Backdop nodes.

Note: If your Drupal 7 site is on a 2.x-dev or 3.x-dev release, you may need to
adapt the upgrade path for your needs. (If you do, please consider contributing
those changes back, to help other people upgrading from the same branch.)


Installation
------------

- Install this module using the official Backdrop CMS instructions at
  https://backdropcms.org/guide/modules.

Documentation
-------------

Additional documentation is located in the Wiki:
https://github.com/backdrop-contrib/biblio/wiki/Documentation.

Issues
------

Bugs and Feature requests should be reported in the Issue Queue:
https://github.com/backdrop-contrib/biblio/issues.

Current Maintainers
-------------------

- [Jen Lampton](https://github.com/jenlampton).
- Seeking additional maintainers.

Credits
-------

- Ported to Backdrop CMS by [Jennifer Hodgdon](https://github.com/jhodgdon).
- Originally written for Drupal by [Derek Wright](https://www.drupal.org/u/dww).
- Maintained for Drupal by [many other fabulous people](https://www.drupal.org/node/69435/committers).

License
-------

This project is GPL v2 software.
See the LICENSE.txt file in this directory for complete text.
