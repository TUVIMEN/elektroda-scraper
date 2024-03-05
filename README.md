# elektroda-scraper

A bash script for scraping elektroda forum to json.

## Requirements

 - [hgrep](https://github.com/TUVIMEN/hgrep)
 - [jq](https://github.com/stedolan/jq)
 - [recode](https://github.com/rrthomas/recode)

## Installation
    
    install -m 755 elektroda-scraper /usr/bin

## Supported links formats
    
    https://www.elektroda.pl
    sitemap
    elektroda
    https://www.elektroda.pl/forum-gf-[0-9]+
    forum-gf-[0-9]+
    forums
    https://www.elektroda.pl/rtvforum/forum[0-9]+.html
    forum[0-9]+
    forum[0-9]+-[0-9]+
    https://www.elektroda.pl/rtvforum/topic[0-9]+.html
    topic[0-9]+
    [0-9]+

## Json format

Here's [json](example.json) from some issue on [elektroda](https://www.elektroda.pl/rtvforum/topic3044759.html)

## Usage

    elektroda-scraper directory [URLS...]

All options should be specified before the directory.

The script writes every question to file in the directory (without overwriting them) and names of the files is the ids of questions.

Download issues from sitemap to directory x

    elektroda-scraper x sitemap

Download issues from forums to directory x

    elektroda-scraper x forums

Download some issues to directory x

    elektroda-scraper x 3044759 924997 3188141 https://www.elektroda.pl/rtvforum/topic3300674.html

Download issues from forum 112 to directory x

    elektroda-scraper x forum112

Get some help

    elektroda-scraper -h
