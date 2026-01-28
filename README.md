## enjoy this little bunch of dev automation scripts
(hopefully it'll make backporting easier)
(every so slightly)

## dev-scripts

1. `git-commit-num <commit_id> <log_file>`
- returns the commit number of a specified commit_id in a specified log_file
  * `<commit_id>`: the commit_id whose commit number you want to search for
  * `<log_file>`: contains a list of numbered commits in the linux master branch.
  * higher the commit number, earlier the commit.
  * `log_file` can be generated using `git log --oneline > log_file`

2. `git-head [n]`
- returns the oneline commit log of specified n commits (10 if unspecified)

3. `git-search-string <string> <filename>`
- returns the list of commits that involve changes in the specifed string in the specified file
  * `<string>`: the string being modified/added/deleted you want to search for
  * `<filename>`: the file across whose commit history you want to search in
 

## how to get them in your system (use them as regular commands from anywhere in your system, any session)
- clone the repo in whichever directory you'd like (but keep track of that path)
- `vim ~/.bashrc`
- go to the bottom of the file and add: `export PATH="$HOME/<your-path>/dev-scripts/bin:$PATH"`
- verify: `which <cmd_name>`
