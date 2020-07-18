= 101GB Zlib Zipbomb Repo

This repo, while only occupying around 224K on disk for servers/mirror repos, expands to around 101GB when cloned normally, as the objects are all 99MB zero filled files, all duplicates. These files, being duplicate, are deduped by git, and then zlib compressed, making the repo look innocuous until cloned.

This principle could be used to create repos of even larger sizes, all to maliciously or as a prankster, burn people's time, CPU resources, ram, and disk space if they have enough to clone the entire repo and expand it in the first place.

Props to https://github.com/Katee/git-bomb for having an equally cool exploit, although it relies more on recursion and folder creation to tie up the works.

Currently pending on github's hackerone. Once allowed, I'll make it public.
