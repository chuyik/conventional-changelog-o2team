# [![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Dependency Status][daviddm-image]][daviddm-url] [![Coverage Status][coveralls-image]][coveralls-url]

**Issues with the convention itself should be reported on the O2Team issue tracker.**

## O2Team Convention

O2Team's [commit message guidelines](https://github.com/O2Team/O2Team/blob/master/CONTRIBUTING.md#commit).

### Examples

Appears under "新功能" header, pencil subheader:

```
feat(pencil): add 'graphiteWidth' option
```

Appears under "问题修复" header, graphite subheader, with a link to issue #28:

```
fix(graphite): stop graphite breaking when width < 0.1

Closes #28
```

Appears under "性能优化" header, and under "Breaking Changes" with the breaking change explanation:

```
perf(pencil): remove graphiteWidth option

BREAKING CHANGE: The graphiteWidth option has been removed. The default graphite width of 10mm is always used for performance reason.
```

The following commit and commit `667ecc1` do not appear in the changelog if they are under the same release. If not, the revert commit appears under the "代码回滚" header.

```
revert: feat(pencil): add 'graphiteWidth' option

This reverts commit 667ecc1654a317a13331b17617d973392f415f02.
```

### Commit Message Format

A commit message consists of a **header**, **body** and **footer**.  The header has a **type**, **scope** and **subject**:

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

The **header** is mandatory and the **scope** of the header is optional.

### Revert

If the commit reverts a previous commit, it should begin with `revert: `, followed by the header of the reverted commit. In the body it should say: `This reverts commit <hash>.`, where the hash is the SHA of the commit being reverted.

### Type

If the prefix is `feat`, `fix` or `perf`, it will appear in the changelog. However if there is any [BREAKING CHANGE](#footer), the commit will always appear in the changelog.

Other prefixes are up to your discretion. Suggested prefixes are `build`, `ci`, `docs` ,`style`, `refactor`, and `test` for non-changelog related tasks.

### Scope

The scope could be anything specifying place of the commit change. For example `$location`,
`$browser`, `$compile`, `$rootScope`, `ngHref`, `ngClick`, `ngView`, etc...

### Subject

The subject contains succinct description of the change:

* use the imperative, present tense: "change" not "changed" nor "changes"
* don't capitalize first letter
* no dot (.) at the end

### Body

Just as in the **subject**, use the imperative, present tense: "change" not "changed" nor "changes".
The body should include the motivation for the change and contrast this with previous behavior.

### Footer

The footer should contain any information about **Breaking Changes** and is also the place to
reference GitHub issues that this commit **Closes**.

**Breaking Changes** should start with the word `BREAKING CHANGE:` with a space or two newlines. The rest of the commit message is then used for this.

A detailed explanation can be found in this [document](#commit-message-format).

[npm-image]: https://badge.fury.io/js/conventional-changelog-o2team.svg
[npm-url]: https://npmjs.org/package/conventional-changelog-o2team
[travis-image]: https://travis-ci.org/conventional-changelog/conventional-changelog-o2team.svg?branch=master
[travis-url]: https://travis-ci.org/conventional-changelog/conventional-changelog-o2team
[daviddm-image]: https://david-dm.org/conventional-changelog/conventional-changelog-o2team.svg?theme=shields.io
[daviddm-url]: https://david-dm.org/conventional-changelog/conventional-changelog-o2team
[coveralls-image]: https://coveralls.io/repos/conventional-changelog/conventional-changelog-o2team/badge.svg
[coveralls-url]: https://coveralls.io/r/conventional-changelog/conventional-changelog-o2team
