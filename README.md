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
- Where 1 is feature name and 2 is what to branch from
