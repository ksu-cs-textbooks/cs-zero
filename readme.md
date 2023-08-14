# Cloning for the first time?

1. `git clone --recursive [URL to Git repo]`
2. or `git clone` and:
   1. `git submodule update --init --recursive`
   2. pull all changes in the repo including changes in the submodules `git pull --recurse-submodules`
   3. pull all changes for the submodules `git submodule update --remote`

Other help: [https://ksucs-hugo.russfeld.me/7-documentation/02-starter/]
(https://ksucs-hugo.russfeld.me/7-documentation/02-starter/)