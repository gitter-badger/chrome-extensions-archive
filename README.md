
# Chrome Extensions Archive

The goal is to provide a complete archive of the chrome web store with version
history.

You can see the current status of what's archived and download the files here:
[dam.io/chrome-extensions-archive/](http://dam.io/chrome-extensions-archive/)

## Installing the extensions

To install an extension, go to `chrome://chrome/extensions/` and drop the file.

To avoid the auto-update, [load it as an unpacked extension](http://stackoverflow.com/a/24577660/1075195)

Files are named as `.zip` but they are the exact same `.crx` stored on the store.

## Running the scripts

Crawling:

- `crawl_sitemap.py`: gets you the list of all the extensions
- `crawl_crx.py`: use `sitemap.json` to download the crx

Site & stats:

- `scan_pages_history_to_big_list.py`: make `PAGES.json` by scanning the pages
you crawled
- `crx_stats.py`: make `crx_stats.json` (what's currently stored)
- `make_website.py`: use `crx_stats.json` + `PAGES.json` to generate the site

For now I rsync the crx directory on Google Cloud Storage directly.

## Helping out

I have a few things in mind for the future:

- diff of extensions versions as a web interface
- malware/adware analysis
- running an alternative web store (better search, firefox support,...)

Don't hesitate to reach out (here on issues, damien@dam.io or @dam_io on twitter)
