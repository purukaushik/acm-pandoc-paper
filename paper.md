# Prerequisites

* A good idea.
* Some references.
* Knowledge of how to use markdown.
* (Optional) `pandoc` installed locally along with `texlive-full`.
* A Github account.

# Steps

First, clone the preconfigured repo.

```bash
git clone git@github.com:Hoverbear/acm-pandoc-paper.git
```

After, create a [new Github repository for your paper](https://github.com/new). Don't add any initialization files. *Note:* Travis CI only offers free workers for public repos.

Then you can visit your [Travis CI Profile](https://travis-ci.org/profile) and switch the repository you created to 'on'. *Hint:* You might need to hit "sync".

Since it would be positively outrageous to give Travis your Github password or private key, we'll use what's called an "access token". To get one of these, go to your Github settings and you need to create a "Personal Access Token", you only need to give it the "public_repo" permission. From there you can install the [Travis Gem](https://github.com/travis-ci/travis.rb#installation) and safely encrypt it. Make sure to delete the existing key from `.travis.yml` first, that's mine!

```bash
travis encrypt GH_TOKEN=$YOUR_TOKEN --add env.global
```

Now, point the repo that was cloned to your newly created Github repository. The easiest way of doing this is:

```bash
rm -rf .git
git init
// Add your things and commit.
git remote add origin $YOUR_REPO
git push -u origin master
```

Now every time you push to the repository Travis will go and build a PDF and HTML output page to the `gh-pages` branch of your repository. Your papers will be at `https://$USER.github.io/$REPO/` and `https://$USER.github.io/$REPO/paper.pdf` respectively.

If you want to see the output on your machine just run `make` and check in `out/`.

You can see the example output [here](https://hoverbear.github.io/acm-pandoc-paper/) and [here](https://hoverbear.github.io/acm-pandoc-paper/paper.pdf)

Currently fixed the multiple author issue.
# References
