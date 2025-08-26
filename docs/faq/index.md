---
title: FAQ
hide:
  - navigation
---

# Frequently Asked Questions

## The Basics

### What is StashDB?

StashDB.org is our shared public instance of the Stash-Box software. It hosts information about a wide variety of scenes, studios, and performers that can be easily pulled into your own installation of Stash. It does not host any video files or link to any unofficial downloads.

Very few users will have reason to host or install a Stash-Box instance themselves, so if you're confused by the terminology just focus on [linking StashDB to your local installation of Stash](LINKZ/accessing-stash-boxes/). Detailed instructions for connecting to StashDB can be found in the pinned messages of our **#stashdb-invites** channel on [Discord](LINKZ/joining-discord-and-matrix/).

### What makes StashDB better?

Full integration with Stash and improved scene matching using various fingerprints (pHashes)

StashDB is not the only source of much of its metadata. When filling out information in Stash, you will likely use multiple sources to cover various parts of your collection. Stash has a helpful [repository of scrapers](https://github.com/stashapp/CommunityScrapers){:target="_blank"} to assist with that. Each source will have its own strengths and weaknesses, just like StashDB. However, the main advantages of using StashDB over similar databases are:

1. **Full continuing integration with Stash.** Stash, Stash-Box, and StashDB are all part of the same shared project. They all enjoy the benefits of parallel development, always keeping each other in mind when creating or updating new features. Updating info in Stash from StashDB should be easier and more versatile than using other sources, just as updating StashDB from within Stash should become more convenient as well.

2. **The ability to match your files with scene entries on StashDB using hashes/fingerprints alone.** With the inclusion of [perceptual hashes](LINKZ/whats-a-phash/), even files of differing resolutions, encodes, or download sources will often be similar enough to still match with StashDB. In other words, your files and their hashes don't have to be exact matches with the fingerprints on StashDB. Stash will be able to find matches as long as your video _looks just similar enough_ to somebody else's fingerprint submission. This level of fuzzy matching makes our system much more reliable, flexible, and versatile than alternative approaches.

### What's a pHash?

Perceptual hashes are generated from what a video looks like, allowing for more reliable scene matching with StashDB.

[Perceptual hashes](https://hackerfactor.com/blog/index.php%3F/archives/432-Looks-Like-It.html){:target="_blank"} (pHashes) are one of the main reasons why we [recommend using StashDB]({{ site.baseurl }}/docs/faq_getting-started/stashdb/what-makes-stashdb-better/) with Stash. pHashes are used to match your video files with scene entries on StashDB. Even files of differing resolutions, encodes, or download sources will often be similar enough to still match with StashDB. In other words, your files and their hashes don't have to be exact matches with the fingerprints on StashDB. Stash will be able to find matches as long as your video _looks just similar enough_ to somebody else's fingerprint submission. This level of fuzzy matching makes our system much more reliable, flexible, and versatile than alternative approaches. pHashes can also be used in Stash to detect duplicate files in your library, using the "Scene Duplicate Checker" in the "Tools" tab of the Settings page.

pHashes are not generated in Stash by default, so you will need to create them yourself. They may be generated during a Scan by activating the switch next to "Generate perceptual hashes" or through the Generate task (in the "Tasks" tab of the Settings page or the "Generate..." option with individual scenes selected) next to "Perceptual hashes (for deduplication)". These may be submitted to existing scenes on StashDB along with other fingerprints using the [Scene Tagger]({{ site.baseurl }}/docs/faq_getting-started/stashdb/using-stashdb/) and will be included automatically when [submitting new scenes via draft]({{ site.baseurl }}/docs/faq_getting-started/stashdb/using-stashdb/).

### What's a StashID?

Unique ID for entries in StashDB, found at the end of URLs and saved to Stash after a match.

A StashID is the unique identifier for an entry on StashDB. It can be found in the URL of a scene/performer/studio entry as the string of seemingly random numbers and letters at the end. StashIDs can be saved to your own scenes, performers, and studios in Stash when using the [Tagger view or Identify function]({{ site.baseurl }}/docs/faq_getting-started/stashdb/using-stashdb/) as well as a Stash-Box scraper. This links your local entries in Stash to their match on StashDB for future reference and scrapes.

As there is no Studio Tagger or studio scraper support, the Scene Tagger view is currently the only way to attach a StashID to a locally saved studio. The Tagger will give you several options to choose from when it doesn't find a studio's StashID saved anywhere locally. From left to right, you can create a new studio with the suggested name and StashID (no other details are saved at this time), skip the studio field entirely, or attach the StashID to a studio you've already created. This last option will be selected automatically if a studio's primary name or an alias exactly match the name of the suggested studio on StashDB. Be sure to click the floppy disk icon to save your selected action, creating the new studio or attaching the StashID.

### Where do I report mis-matched fingerprints?

Not everything can be fixed directly from StashDB's UI. For these exceptions, we have a spreadsheet hosted on Google Sheets to log corrections until they can be handled at a later date. There are several pages in the backlog, so make sure you find the correct one. Its most common use right now is to log incorrect fingerprints.

[Our backlog spreadsheet can be found here.](https://docs.google.com/spreadsheets/u/0/d/1eiOC-wbqbaK8Zp32hjF8YmaKql_aH-yeGLmvHP1oBKQ/edit){:target="_blank"}

### Why do some images on StashDB appear broken?

Be sure to disable your browser's ad-blocker for StashDB's domain, or add the domain to the allow/white list. StashDB does not host ads of any kind, but some image URLs will get false-flagged as advertisements and will fail to load. These images will appear to be broken on the webpage.

---

## Editors

### What are "unconfirmed" guidelines?

Many of this guidelines on this website will include the following message:

!!! warning ""

    Unconfirmed guideline, subject to change pending formal approval.

This just means the language has not been formally approved yet. Instead, each one represents a working consensus developed organically between contributors over time.

Contributors are still expected to follow and enforce these unconfirmed guidelines, but should know that they are subject to change in the near future. Continually violating them may still result in the [removal of edit access]({{ site.baseurl }}/docs/faq_getting-started/edits/moderation-enforcement/).

---

## Performers

### I found a profile containing scenes from multiple performers with the same name. What should I do?

Many performer entries are considered "ambiguous", with multiple performers sharing the same entry on StashDB. This happens most often to single names with no last name or initial, for example "Anna" or "Tony". Currently, the only way to handle these is to reassign the performer on every scene individually which can be tedious and time-consuming. This also often requires the creation of multiple performer entries that do not exist separately yet, which slows down the process even more.

There have been proposals to split these problem entries into multiple performers by studio/network to speed up the process with simple merges, but this method is not possible yet.

### How does StashDB decide the order of performer images? Is there a way to manually rearrange them?

Images are currently ranked by size. This means the vertical image (portrait orientation) with the largest resolution is shown first, with the rest in descending order. Any horizontal images (landscape orientation) come last, also descending in size. This means images that may be considered too small to be useful can be easily found toward the end of the line.

There have been suggestions to instead sort performer images by popularity, allowing users to upvote and downvote individual images. That would allow us to collectively decide which one looks best as the primary image, but this method is not possible yet.

---

## Scenes

### Duplicate Scenes

{: .important }
**Search using keywords, filters, and pHashes.**

Before submitting a scene to StashDB, always check for duplicates first. Duplicates will [likely be rejected or removed]({{ site.baseurl }}/docs/scenes/create/duplicate-scenes/). If you couldn't find a match through Stash's [Scene Tagger]({{ site.baseurl }}/docs/faq_getting-started/stashdb/using-stashdb/), the easiest way to check is to rely on [pHash]({{ site.baseurl }}/docs/faq_getting-started/stashdb/whats-a-phash/) detection when [submitting a draft]({{ site.baseurl }}/docs/faq_getting-started/stashdb/using-stashdb/) to StashDB. Your draft edit will have a warning sign (⚠) at the top if your pHash matches existing scenes in the database. These are not always duplicate scenes and may be due to someone [submitting incorrect fingerprints]({{ site.baseurl }}/docs/faq_getting-started/stashdb/backlog-spreadsheet/). Duplicates may also be found by searching for the title on StashDB or by filtering by studio on a performer's page. Also be aware that even if your scene isn't on StashDB yet, someone could have a pending edit to create the same scene. Best way to check for this is to click the favorite star (⭐) on the relevant studio or performer in your submission and [filter for favorites in pending scene creations](https://stashdb.org/edits?favorite=true&operation=create&status=pending&type=scene){:target="_blank"} on the Edits page.

### Check Performers

{: .important }
**Find missing performers and avoid ambiguous entries.**

When submitting a new scene, make sure that you are not [missing any performers]({{ site.baseurl }}/docs/scenes/edit/scene-performers/missing-performers/). If they are listed on the studio page, in the title, or in the description, you will be expected to include them in your submission. Also make sure that none of your included performers link to [ambiguous performer entries]({{ site.baseurl }}/docs/faq_getting-started/performers/ambiguous-performers/). These are most often single-name performers with nothing in their disambiguation field. Both of these may put your scene creation at risk of being rejected.

---

## Studios

### Duplicate Studios

{: .important }
**Search using keywords on "Studios" page.**

Before adding a new studio, make sure it doesn't already exist by searching [StashDB's list of studios](https://stashdb.org/studios){:target="_blank"}. Additional search terms will expand the list of results on that page right now, so try to limit yourself to the most unique search term in your studio's name. Also, be aware of our other policies for [creating studios]({{ site.baseurl }}/docs/studios/create/) that may be relevant.

### Check Image Size

{: .important }
**Large images (greater than 1280px in either dimension) are automatically downscaled, which may remove transparency from PNGs.**

Images uploaded to StashDB will be downscaled to no greater than 1280 pixels in either dimension. Due to an old bug, PNGs may be converted to JPGs when downscaling. This means that studio images might lose any transparency they may have if it's over 1280 pixels tall or wide. While this bug has been fixed for most users, it may still affect the occasional file. You may need to manually downscale transparent images to fit these size requirements before uploading them to StashDB if it becomes a problem.

---

## Tags

### Read Tag Edit Histories

{: .important }
**Comments in the "Edits" tab will often explain why a tag is organized a certain way, so check it first before making an edit.**

If you're wondering why a tag is named/defined/organized a certain way, often the answer is in its edit history. In a tag's detail page, click on the "Edits" tab underneath its list of aliases. The comments on these edit submissions often explain the reasoning behind them, sometimes at great length. If you feel like a tag needs to be changed or merged in some way, please look through these edit comments first. They may show you that an idea has already been considered and explain why it hasn't been implemented.

### Check Tag Usage

{: .important }
**Look at the scenes underneath a tag to get an idea of its current usage before submitting a destructive edit or description change.**

Before submitting an edit to a tag, always look through the scenes underneath it first. Most tags are defined to [match their current usage]({{ site.baseurl }}/docs/faq_getting-started/tags/scraped-vs-manual-tags/), so you will need to have a good idea of how it's currently used before you can make an informed decision about how it should be handled. If you're trying to write a new definition for a tag that's missing one, you may find that its scenes are using that tag differently than what you assumed. A tag's current usage, the consistency of its usage, the source of its scenes, and its total number of scene entries will all factor into decisions regarding possible edits.

### Scraped vs. Manual Tags

{: .important }
**Most tags attached to scenes were scraped from studio sources, not manually added by editors.**

Currently, most tags attached to scenes are scraped from the original studio or some other official source, not manually added from the editors of StashDB. Our current methods of manually adding/removing a scene's tags individually isn't too bad on a small scale, but they are far too tedious and time-consuming to be worth using for large shifts in our tag organization in most cases. This means that most of StashDB's tag list leans on scraped tags in their organization and usage, rather than attempting to enforce major deviations from those sources. This may explain inaccuracies, inconsistencies, or other peculiarities of a particular tag. [Reading through the edit comments]({{ site.baseurl }}/docs/faq_getting-started/tags/read-tag-edit-histories/) may explain in further detail.

### Sorted vs. Unsorted Tags

{: .important }
**Tags without categories and/or descriptions are considered "unsorted" and should generally be avoided when manually adding tags to scenes.**

If a tag doesn't have a category or description, then it is likely still unsorted. It will usually have a sparse or non-existent edit history as well. This means it's exact usage hasn't been determined yet, no potential merge targets have been found, and no decision has been made on if it's even worth keeping. It's usually preferable to avoid unsorted tags when manually adding them to a scene yourself. If you're just adding scraped tags though, don't worry if they're currently sorted or unsorted. More scraped sources for an unsorted tag could help us decide what to do with it in the future. Finally, if you want to find a quick list of sorted tags, lean on the [Tag Categories page of StashDB](https://stashdb.org/categories){:target="_blank"}. Every tag with a category assigned will be organized to some extent already.

### Merging and Destroying Tags

{: .important }
**Unsorted tags that do not have a unique and helpful meaning are candidates for merging/deleting.**

Great care must be taken when merging or deleting tags. When tags are merged or destroyed, it is not easily reversed. Currently, the goal when handling unsorted tags is consolidation. We are aiming to merge all closely related tags together while deleting any that are considered extraneous. The purpose is to create a curated set of tags that are as helpful and as consistent as possible, spanning every studio on StashDB. Just like with other parts of the database, merging is always preferred over deleting. Candidates for a merge/deletion could be tags that seem too vague, too specific, or otherwise irrelevant. These are of course subjective calls, but the rule of thumb should be, "Does this tag have a unique and helpful meaning?" If the answer is "yes", then keep it. If it's "no", then merging/deleting may be the best option. However, we are still trying to be conservative in our approach. Reverting changes can be tricky, so it's better to err on the side of keeping a tag if there's any doubt. Merges should also aim for a resulting tag that is consistent in its meaning. If the inclusion of a tag would result in less consistency of meaning, then it may be best to leave it separate for now. Finally, please remember to include any merged tag names [as aliases]({{ site.baseurl }}/docs/tags/edit/tag-aliases/adding-tag-aliases/). This can be done in your merge submission.
