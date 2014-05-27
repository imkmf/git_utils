# git_utils

A nice collection of git utilities written in pure bash.

Note that a lot of these are provided by Git, but are wrapped in bash functions so you don't have to remember a bunch of optargs and things like that.

---

- is_git

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

- number_of_commits

Number of commits for a repository.

```
number_of_commits
118
```

- top_commits_by_author

Top commits by author.

```
top_commits_by_author

115 Kristian Freeman
30  <someone>
10  <other people, contrived example lololol>
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
