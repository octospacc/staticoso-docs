# [staticoso:Site:Name]

Don't yet mind the fact that there is no CSS at all, and only one single page. Still a heavy WIP :)


## Input Files

### Templates and Parts

For templates and parts files, currently only HTML is supported.

### Pages and Posts

For pages and posts files, many formats are supported as input:

- Markdown (Suffixes: `.md`)
- Pug (through pug-cli) (Suffixes: `.pug`)

Some are planned for support, but some bugs have to be fixed fist:

- HTML (Suffixes: `.htm`, `.html`)
- Plain text (Suffixes: `.txt`)


## Site folder Structure

A typical staticoso site folder looks like this:

- `Assets/`: Contains files that will be just copied as they are in the root of the output folder.
- `Pages/`: Contains website pages.
- `Posts/`: Contains website posts, which differ for some things from pages.
- `Templates/`: Contains base HTML pages to be used as templates for compiling all the pages.
- `StaticParts/`: Contains HTML snippets that can be included statically in HTML templates.
- `DynamicParts/`: Contains HTML snippets that can be included dynamically, via configuration flags, in HTML templates. 
- `Site.ini`: Specifies some configuration flags.


## Configuration Flags

Many configuration flags are available.

They can be specified from the `Site.ini` file, under the `[Site]` section, or as command-line arguments.  
CLI arguments, if specified, always take priority over the INI values.

In the INI file, flags are specified as they are, separated by new lines. In 

_Note: Some flags are currently CLI-only, while others are file-only. This will be soon fixed._

- `SiteName`: The name of your site.
- `BlogName`: The name of the blog section of your site.
- `SiteTagline`: The tagline or motto of your site.
- `SiteRoot`: The root path of your site on your server. Defaults to `/`.
- `SiteDomain`: Domain of your website, for use for feeds and sitemaps.
- `SiteLang`: The language of your site. Will be used for choosing certain strings. Defaults to `en`.
- `SiteTemplate`: Name of the template file to use for the site. Defaults to `Default.html`.

- `Minify`: Whether or not to minify the output HTML. Defaults to `False`.
- `NoScripts`: Whether or not to strip out `<script>` tags from the output HTML. Defaults to `False`.
- `Sorting`: -

- `GemtextOut`: Whether or not to output a Gemtext conversion of the site. Requires html2gmi. Defaults to `False`.
- `GemtextHeader`: A string to optionally include at the top of every Gemtext file.

- `SitemapOut`: Whether or not to create sitemap files. Defaults to `True`.
- `FeedEntries`: Max number of pages to include in feed files. A value of `0` disables feed generation, while `-1` equals no limit. Defaults to `10`.
- `FolderRoots`: -
- `DynamicParts`: -
- `MarkdownExts`: -
- `MastodonURL`: URL of a Mastodon instance to use for notifying of new posts and creating comment links. Leave blank to disable Mastodon.
- `MastodonToken`: Application token of a Mastodon account to use for notifying of new posts and creating comment links. Leave blank to disable Mastodon.
- `FeedCategoryFilter`: -
- `ActivityPubTypeFilter`: -
- `ActivityPubHoursLimit`: -
- `AutoCategories`: Whether or not to automatically create pages in the `Categories/` directory of your site. Defaults to `False`.

