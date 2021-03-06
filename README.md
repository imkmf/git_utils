# git_utils

A nice collection of git utilities written in simple Bash or sometimes Ruby.

Note that a lot of these are provided by Git, but are wrapped in bash functions so you don't have to remember a bunch of optargs and things like that.

---

#### is_git

Check if current directory is in a git repository.

`-s` will return a status code: "0" for a git repo, "128" if not. Echo `$?` to see the response:

```
is_git -s
echo $?
0
```

`-v` will return "TRUE" or "FALSE", along with the status code:

```
is_git -v
TRUE
echo $?
0
```

#### number_of_commits

```
number_of_commits
118
```

#### top_commits_by_author

```
top_commits_by_author

115 Kristian Freeman
30  <someone>
10  <other people, contrived example lololol>
```

#### minutes_since_last_commit

```
minutes_since_last_commit
5
```

#### time_since_last_commit

```
time_since_last_commit
about 16 hours
```

*Note that this utilizes a helper from [action_view](https://rubygems.org/gems/actionview) so you'll want a functioning Ruby/Rails installation for this.*

#### last_commit_time

```
last_commit_time
Tue May 27 10:54:46 2014 -0700
```

#### initialize_repo

Initializes a repo with `git init` in the current directory, then adds all files and does a initial commit. Unless given an `$1` (single argument), the `$REPO` variable will be set to the current directory.

```
initialize_repo
"Initial commit for $REPO"
```

### Contributing

Issues/PRs welcome – this is a PoC mostly for things that I find handy, but new things are obviously welcome.

### License

    The MIT License (MIT)

    Copyright (c) Kristian Freeman 2014

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in
    all copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
    THE SOFTWARE.
