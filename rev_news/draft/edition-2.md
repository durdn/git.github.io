
## Git Rev News: Edition 2 (April 15, 2015), 10 years of Git & Git Merge 2015!

Welcome to the second edition of [Git Rev News](http://git.github.io/rev_news/rev_news.html),
a digest of all things Git, written collaboratively
on [GitHub](https://github.com/git/git.github.io) by volunteers.

Our goal is to aggregate and communicate
some of the activities on the [Git mailing list](mailto:git@vger.kernel.org)
in a format that the wider tech community can follow
and understand. In addition, we'll link to some of the interesting Git-related
articles, tools and projects we come across.

This special edition covers Git's 10th anniversary and
the [Git Merge 2015](git-merge.com) on April 8th & 9th in Paris, France,
where many Git fans celebrated this anniversary. 

You can contribute to the upcoming edition by sending [pull
requests](https://github.com/git/git.github.io/pulls) or opening
[issues](https://github.com/git/git.github.io/issues).

## Discussions

### General

* [10 years of fun](https://docs.google.com/presentation/d/1sc1xsG9vrRahcckD8WwYeK355SvQH7NSchKH07icJtk/pub)

At the Git Merge 2015, Junio Hamano started the Contributor
Summit by giving a presentation called "10 years of fun with Git" and
saying that he wanted to take advantage of the 10th anniversary to
thank the contributors.

He showed how the first initial revision of Git, created on the 7th of
April 2015 by Linus, looks like, and compared it to a recent
revision. Though its size is around 0.2% of the size of a recent
revision, the initial revision is enough to start using Git.

An interesting question is then "Who made today's Git?" and to answer
that question Junio gave the results of many different queries.

For example to get a commit count sorted by author and excluding merge
commits, one can use:

```
git shortlog --no-merges -n -s v2.4.0-rc0
```

With the results of each such query, Junio gave insights about how we
can interpret the results, told about caveats that might apply, and
also took time to thank the people who appear in these results.

Towards the end of the presentation he also told about people who
didn't appear in the results: bug reporters, feature wishers,
reviewers and mentors, alternative implementors and porters, trainers
and evangelists. And he assigned to this news letter the tasks of
talking about and thanking them all ;-)

* [Git Large File Storage](https://git-lfs.github.com/)

At the Git Merge 2015, Rick Olson, a developer working for GitHub also
known as @technoweenie, gave a presentation about Git Large File
Storage (Git LFS).

On the Git Merge web site the name of the presentation is "Building a
Git Extension with First Principles" probably because GitHub didn't
want to announce Git LFS a long time before the conference. In fact it
was announced [first on The GitHub Blog](https://github.com/blog/1986-announcing-git-large-file-storage-lfs)
the day before the presentation.

Rick started by explaining the reasons why such an extension was
needed, namely that Git starts to suck with large binary file
objects. For example it takes longer and longer to clone a repo that
has more and more of such objects.

Then he told that GitHub did some user experience research with a
diverse team of users with this problem. They also experimented with
existing solutions like `git media` and `git annex`.

Rick then detailed [the solution that was
implemented](https://github.com/github/git-lfs/blob/master/docs/spec.md)
using the Go language, and how it can be used, with commands like:

```
git lfs init
git lfs track "*.zip"
git lfs push
```

Remote configuration, the server side, the Git LFS API and authentication were also
covered. And in the end Rick talked about some ideas for improvements.

### Reviews

### Support

## Releases

## Other News

### Events

* [Git Merge 2015](http://git-merge.com/), The Conference for the Git
Community, took place on April 8th & 9th in Paris, France. It was presented by
GitHub with sponsorship from Microsoft and Atlassian. Scott Chacon (GitHub),
wearing a beautiful suit, was the master of ceremony on the 9th of April, while
Chris Kelly and other GitHub people had organized everything.
Thanks to them and the sponsors for this great time!
The following resources emerged from the event:
  * TODO: Link to YouTube videos of recorded talks?

### Media

* 10 years ago, [Linus' first ever mention of what would become Git
  ](https://news.ycombinator.com/item?id=9264088)
* As Google Code shuts down, the [Vim project decides moving to Git/GitHub
  ](https://news.ycombinator.com/item?id=9263193)
* [Nice, SVG-based Git cheat sheet
  ](https://rawgit.com/pastjean/git-cheat-sheet/master/git-cheat-sheet.svg)
* Mary Rose Cook has written an essay on [Git from the inside out
  ](http://maryrosecook.com/blog/post/git-from-the-inside-out)
* A similar article from last year: [Git from the Bottom Up
  ](https://jwiegley.github.io/git-from-the-bottom-up/), by John Wiegley
* With Git Merge 2015 taking place in Paris, coincidentally the [French Civil
  Code is now on GitHub](https://github.com/steeve/france.code-civil)
* Øyvind A. Holm has generated statistics on the [relative growth of Git repos
  vs. other source control systems](https://github.com/sunny256/openhub-repositories)
* A [Git Style Guide](https://github.com/agis-/git-style-guide) by Agis
  Anastasopoulos
* linux.com's Linus interview, on [10 years of Git
  ](http://www.linux.com/news/featured-blogs/185-jennifer-cloer/821541-10-years-of-git-an-interview-with-git-creator-linus-torvalds)
* Continuing their celebration, a whole series of Git Success Stories have been
  published on linux.com:
  * Wine Maintainer [Alexandre Julliard](https://www.linux.com/news/featured-blogs/200-libby-clark/822789-git-success-stories-and-tips-from-wine-maintainer-alexandre-julliard)
  * Puppet Labs' [Michael Stahnke](https://www.linux.com/news/featured-blogs/200-libby-clark/822555-git-success-stories-and-tips-from-puppet-labs-michael-stahnke)
  * Tor Chief Architect [Nick Mathewson](https://www.linux.com/news/featured-blogs/200-libby-clark/822528-git-success-stories-and-tips-from-tors-chief-architect-nick-mathewson)
  * Drupal Core Committer [Angie Byron](https://www.linux.com/news/featured-blogs/200-libby-clark/822227-git-success-stories-and-tips-from-drupal-core-committer-angie-byron)
  * Qt Maintainer [Thiago Macieira](https://www.linux.com/news/featured-blogs/200-libby-clark/821948-git-success-stories-and-tips-from-qt-maintainer-thiago-macieira)
  * KVM Maintainer [Paolo Bonzini](https://www.linux.com/news/featured-blogs/200-libby-clark/821899-git-success-stories-and-tips-from-kvm-maintainer-paolo-bonzini)
* Some [hefty discussion is going on regarding the new Git Large File Storage](
    https://news.ycombinator.com/item?id=9343021), announced [by GitHub
    ](https://github.com/blog/1986-announcing-git-large-file-storage-lfs) during
    [Git Merge 2015](http://git-merge.com/)

## Credits

This edition of Git Rev News was curated by Christian Couder &lt;<christian.couder@gmail.com>&gt;, Thomas Ferris Nicolaisen &lt;<tfnico@gmail.com>&gt; and Nicola Paolucci &lt;<npaolucci@atlassian.com>&gt; with help from ???.
