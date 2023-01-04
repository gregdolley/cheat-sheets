# Git

## The Basics

|Command|Description|
|:---|:----|
|```git init```|Creates a git repository in the current directory.|
|```git init <directory>```|Creates and git repository in the specified directory.|
|```git commit -m "<message>"```|Commits everything that is currently in the staged snapshot. Use \<message\> for the commit message. To add a long description to the commit message, don't type the ending quote - instead press \<Enter\> and type the description on the next line (you can hit \<enter\> for however many line breaks are needed in the long description). Type the ending quote at the end of the long description and hit \<Enter\> again. This send everything to git in one command and it will parse out the short commit message from the long description.|

## Shortcuts

|Command|Description|
|:---|:----|
|```git add --patch```| Launches git into "interactive" mode and goes through every new change and displays hunks of them at a time asking you whether to stage or not stage each hunk. You can also choose to do a manual edit of a hunk before staging it - very useful if you need to make a small correction on something, or maybe you want to stage only the "code part" of a hunk, and exclude commented lines that only applied to you and your dev environment (this way you get to keep your dev specififc comments only in your version of the codebase).|

## Advanced

|Command|Description|
|:---|:----|
|```git format-patch <commit/branch_name>```|Creates individual patch files, one for each commit, which are meant to be applied to a local repo which is only current up to the specified \<commit\> or has the most up-to-date commit of <branch_name>, but is behind all the commits of the repo this command is run against. These patch files are ordered based on the number prefix of their filename - first one starts at "0000-", the second at "0001-", and so on. When all patch files are applied in order to the local repo, git basically recreates all the code/file/folder changes specified in the patch files and brings the local repo up-to-date with the HEAD of the repo where the patch files originated.|
| ```git format-patch <commit/branch_name> --stdout > all_commits.patch```|This command does the identical operation as the one above (meant to create a patch for an out-of-date repo and bring it current with the repo this command is run against), except instead of creating individual patch files, this command combines all of the patched commits into one single easy-to-use file! No need to worry about file ordering - just import the file generated from this command and be done!|
