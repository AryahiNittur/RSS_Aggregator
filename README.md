# RSS_News_Aggregator

This project reads multiple RSS feeds and generates a structured set of HTML pages. It includes an index HTML page with links to individual feed pages, which themselves contain tables of links to news items from the respective RSS feeds.

## Features

- **Multi-Feed Support**: Reads multiple RSS v2.0 feeds from an XML file and processes each feed.
- **HTML Output**:
  - Generates a main index HTML page with links to individual feed pages.
  - Creates an HTML page for each RSS feed, displaying links to news items in a table.
- **Dynamic Titles and Links**:
  - Uses the input XML's `<feeds>` `title` attribute for the index page title.
  - Displays feed names and links dynamically based on input XML attributes.

## Input Format

The program expects an XML file with the following structure:
```xml
<feeds title="Title for index page">
  <feed url="the feed source URL" name="name of feed for index page"
    file="name of HTML file for feed" />
  <feed url="..." name="..." file="..." />
  ...
</feeds>
