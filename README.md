# Video Ripping Tools: CreateFolders

For convenience, I recently started ripping my DVDs to digital videos, using Handbrake to perform the rip, and MetaX to add appropriate metadata so they can be added to iTunes and not look out of place.

For movies this is fairly straightforward. However, for TV shows, juggling all the output files and simplifying running them through MetaX took a bit of thought. Ultimately I came up with a couple of utilities to help reduce the pain of ripping a full season (or more) of a show.

These were originally written in Perl, but it seemed worthwhile rewriting them in Go and making them available for anyone else who might want them.

## CreateFolders

The first step is to create folders into which each disk of your series can be ripped.

CreateFolders.exe prompts for three pieces of information: series name, number of seasons, and number of disks per season. It will then create a folder tree structure containing one folder per disk per season, under the parent series folder. Each disk in the series should be ripped into the appropriate folder.

## SortByFolder

See the [SortByFolder](https://github.com/PJSoftware/go-sort-by-folder) repo.

## History

Both of these tools were initially developed in my `Command-Line-Util` repo -- an approach guided by my SVN experience. However, multiple projects in a single repo is not the `git` way, so I've finally decided to split them.
