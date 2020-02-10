The Biblio module reproduces some, but not all, of the functionality of the
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

REQUIREMENTS
------------

This module requires the following contributed modules:
- Multifield (machine name: multifield)
- Field Group (field_group)

If you want to be able to import bibliographic information, you will also need:
- Feeds (feeds) -- development version, or release after 1.x-1.0.0-beta, with
  this issue fixed: https://github.com/backdrop-contrib/feeds/issues/10
- Feeds XPath Parser (feeds_xpathparser)
- Job Scheduler (job_scheduler) -- required by Feeds, but not used directly