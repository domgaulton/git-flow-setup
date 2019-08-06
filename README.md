# git-flow-setup

## 1. Setup repository on git

```
echo "# git-flow-setup" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:domgaulton/git-flow-setup.git
git push -u origin master
```

## 2. Set up Git Flow

- Install with Homebrew `brew install git-flow-avh`
- Then in project file `git flow init`

```
Which branch should be used for bringing forth production releases?
   - master
Branch name for production releases: [master]
Branch name for "next release" development: [develop]

How to name your supporting branch prefixes?
Feature branches? [feature/]
Release branches? [release/]
Hotfix branches? [hotfix/]
Support branches? [support/]
Version tag prefix? []
```

## 3. Set up develop branch

This is needed for your first PR to manage it against develop

- `git branch develop`
- `git push -u origin develop`

## 4. Making a new feature

- `git flow feature start [name-of-feature](1) [develop](2)`
- Where 1 is feature name and 2 is what to branch from (develop is default with git-flow)

## 5. Pull Request

- When you commit and push terminal will give you a pull request URL e.g. https://github.com/domgaulton/git-flow-setup/pull/new/feature/git-flow-init-readme
- Make sure you select the PR against develop (not master) as we can manage these releases to develop and later to master

## 6. Release branch

- Once develop has acquired enough features for a release (or a predetermined release date is approaching), you fork a release branch off of develop.
- Start release branch `git flow release start 0.1.0`
- Publish release branch `git flow release publish 0.1.0` so that other developers can merge to it
- Once you have files ready for `master` push above and create PR with github then merge
