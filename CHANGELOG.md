# Release notes

<!-- do not remove -->

## 2.1.2

### New Features

- use global defaults instead of respecifying each time ([#770](https://github.com/fastai/nbdev/pull/770)), thanks to [@seeM](https://github.com/seeM)
- `get_config` works without a settings file ([#768](https://github.com/fastai/nbdev/pull/768)), thanks to [@seeM](https://github.com/seeM)
- add site url ([#767](https://github.com/fastai/nbdev/pull/767)), thanks to [@hamelsmu](https://github.com/hamelsmu)
- add `show_src` to display rich source code ([#763](https://github.com/fastai/nbdev/pull/763)), thanks to [@seeM](https://github.com/seeM)
- add support for `#|exports` ([#762](https://github.com/fastai/nbdev/issues/762))
- `nbdev_merge` prints info like `git merge` ([#753](https://github.com/fastai/nbdev/issues/753))
- helpers to convert fp front matter to quarto front matter ([#750](https://github.com/fastai/nbdev/pull/750)), thanks to [@hamelsmu](https://github.com/hamelsmu)
- Streamline default settings ([#747](https://github.com/fastai/nbdev/issues/747))
- Config keys (and their defaults) should all be documented in one place
- add `user` option to `jupyter_hooks` setting ([#738](https://github.com/fastai/nbdev/pull/738)), thanks to [@seeM](https://github.com/seeM)
- Add appropriate `output-file` to existing frontmatter ([#728](https://github.com/fastai/nbdev/issues/728))

### Bugs Squashed

- `nbdev_prepare` sometimes throws BrokenProcessPool error on MacOS ([#731](https://github.com/fastai/nbdev/issues/731))
- Incorrect relative import from package root inside nested module ([#773](https://github.com/fastai/nbdev/issues/773))
- Jupyter hooks break in environments without `nbdev` installed ([#760](https://github.com/fastai/nbdev/issues/760))
- `nbdev_fix` breaks with empty `ours` patch ([#752](https://github.com/fastai/nbdev/issues/752))
- fix `nbdev_merge` during rebase; fix `nbdev_fix` `nobackup` default ([#737](https://github.com/fastai/nbdev/pull/737)), thanks to [@seeM](https://github.com/seeM)
- non-notebooks do not have nbformat field ([#732](https://github.com/fastai/nbdev/pull/732)), thanks to [@dleen](https://github.com/dleen)


## 2.1.1

### New Features

- add tools from fastrelease to nbdev ([#733](https://github.com/fastai/nbdev/issues/733))

### Bugs Squashed

- fix `nbdev_test` with no `--fname` in non-nbdev repos ([#730](https://github.com/fastai/nbdev/pull/730)), thanks to [@seeM](https://github.com/seeM)
- Auto-generated showdoc headers not in ToC ([#703](https://github.com/fastai/nbdev/issues/703))


## 2.1.0

### Breaking Changes

- `nbdev_sidebar` now looks for `.qmd` files instead of `.md` files

### New Features

- automatically add `output:asis` for showdoc cells ([#726](https://github.com/fastai/nbdev/issues/726))
- accelerate `nbdev_readme` ([#715](https://github.com/fastai/nbdev/issues/715))
- deterministic `show_doc` and `DocmentTbl` `repr` ([#707](https://github.com/fastai/nbdev/pull/707)), thanks to [@seeM](https://github.com/seeM)

### Bugs Squashed

- KeyError 'repo' when trying to create a new nbdev project with `nbdev_new` ([#720](https://github.com/fastai/nbdev/issues/720))
- `show_doc` ends the details column at any `|` character ([#712](https://github.com/fastai/nbdev/issues/712))
- only add to `.gitattributes` if missing ([#706](https://github.com/fastai/nbdev/pull/706)), thanks to [@seeM](https://github.com/seeM)


## 2.0.7

### New Features

- git merge hooks: automatically resolve conflicts and render markers as separate cells ([#704](https://github.com/fastai/nbdev/pull/704)), thanks to [@seeM](https://github.com/seeM)
- Allow clean to keep some metadata keys ([#672](https://github.com/fastai/nbdev/pull/672)), thanks to [@dleen](https://github.com/dleen)
- enable mac terminal install instead of visual installer ([#705](https://github.com/fastai/nbdev/pull/705)), thanks to [@hamelsmu](https://github.com/hamelsmu)
- Conditional content for markdown vs HTML for README ([#694](https://github.com/fastai/nbdev/pull/694)), thanks to [@hamelsmu](https://github.com/hamelsmu)
- Export a single module ([#652](https://github.com/fastai/nbdev/issues/652))

### Bugs Squashed

- Re-enable Mac CI [#425](https://github.com/fastai/nbdev/issues/425))


## 2.0.6

### New Features

- new jupyter save hook to clean NBs ([#697](https://github.com/fastai/nbdev/issues/697)), thanks to [@seeM](https://github.com/seeM)
- new directive `exec_doc` to auto-exec cell when building docs ([#699](https://github.com/fastai/nbdev/issues/699))
- automatically escape YAML strings for title and description in frontmatter ([#691](https://github.com/fastai/nbdev/issues/691))
- add `unbump` param to `nbdev_bump_version` ([#689](https://github.com/fastai/nbdev/issues/689))
- install ghapi automatically ([#690](https://github.com/fastai/nbdev/issues/690))


## 2.0.5

### New Features

- add `nbdev_readme` ([#688](https://github.com/fastai/nbdev/issues/688))


## 2.0.4

### New Features

- add `readme_nb` config option ([#668](https://github.com/fastai/nbdev/issues/668))

### Bugs Squashed

- `exporti` cells can cause showdocs exec to fail ([#679](https://github.com/fastai/nbdev/issues/679))
- missing .html suffix in links ([#674](https://github.com/fastai/nbdev/issues/674))
- Add early return ([#670](https://github.com/fastai/nbdev/pull/670)), thanks to [@dleen](https://github.com/dleen)


## 2.0.0

- From-scratch rewrite of nbdev! nbdev now uses [Quarto](https://quarto.org/) to create beautiful and full-featured websites
- nbdev2 is much faster than previous versions
- Note that you should run `nbdev_migrate_directives` after upgrading to use the new comment directive format (e.g `#| export` instead of `#export`)


## 1.2.11

### New Features

- support py310 style union annotations ([#636](https://github.com/fastai/nbdev/pull/636)), thanks to [@seeM](https://github.com/seeM)

### Bugs Squashed

- fix `show_doc` for properties ([#635](https://github.com/fastai/nbdev/pull/635)), thanks to [@seeM](https://github.com/seeM)
- `nbdev_nb2md` throws error when called in a notebook ([#381](https://github.com/fastai/nbdev/issues/381))


## 1.2.10

### New Features

- Added webrick spec to Gemfile. ([#615](https://github.com/fastai/nbdev/pull/615)), thanks to [@MarkB2](https://github.com/MarkB2)
- Change doc() default for docments ([#611](https://github.com/fastai/nbdev/pull/611)), thanks to [@muellerzr](https://github.com/muellerzr)
- Better checks for cls and self ([#596](https://github.com/fastai/nbdev/pull/596)), thanks to [@muellerzr](https://github.com/muellerzr)
- Use the kernel defined in the kernelspec ([#594](https://github.com/fastai/nbdev/pull/594)), thanks to [@dleen](https://github.com/dleen)
- Add in repr for delegates ([#589](https://github.com/fastai/nbdev/pull/589)), thanks to [@muellerzr](https://github.com/muellerzr)

### Bugs Squashed

- Keep module in name when getting the "qualname" ([#606](https://github.com/fastai/nbdev/pull/606)), thanks to [@muellerzr](https://github.com/muellerzr)
- Fix decimal bug ([#604](https://github.com/fastai/nbdev/pull/604)), thanks to [@muellerzr](https://github.com/muellerzr)
- Use the kernel defined in the kernelspec ([#594](https://github.com/fastai/nbdev/pull/594)), thanks to [@dleen](https://github.com/dleen)
- Misc bug fixes + tests ([#593](https://github.com/fastai/nbdev/pull/593)), thanks to [@muellerzr](https://github.com/muellerzr)


## 1.2.9

### New Features

- Implement `show_doc` for dataclass ([#622](https://github.com/fastai/nbdev/pull/622)), thanks to [@MarkB2](https://github.com/MarkB2)

### Bugs Squashed

- Fix show doc for object, class methods. ([#621](https://github.com/fastai/nbdev/pull/621)), thanks to [@v-ahuja](https://github.com/v-ahuja)
- Fix show doc for keywords. ([#619](https://github.com/fastai/nbdev/pull/619)), thanks to [@v-ahuja](https://github.com/v-ahuja)
- Including `@dataclass` breaks `nbdev_build_lib` ([#595](https://github.com/fastai/nbdev/issues/595))
- `nbdev_nb2md` throws error when called in a notebook ([#381](https://github.com/fastai/nbdev/issues/381))


## 1.2.7

### Bugs Squashed

- Don't build NBs with no `#default_exp`

## 1.2.6

### New Features

- `nbdev_build_libs` now works on a single file even without a `settings.ini` or any `#default_exp` cell
- Handle `#|` as directive prefix

### Bugs Squashed

- nbdev_nb2md throws error when called in a notebook ([#381](https://github.com/fastai/nbdev/issues/381))


## 1.2.5

### New Features

- Update dependencies


## 1.2.3

### Bugs Squashed

- Pin jinja2 due to deprecation bug in nbconvert

## 1.2.2

### New Features

- Update dependencies


## 1.2.1

### New Features

- Make sure docments have linking capability ([#585](https://github.com/fastai/nbdev/pull/585)), thanks to [@muellerzr](https://github.com/muellerzr)
- better logging for duplicate titles ([#584](https://github.com/fastai/nbdev/pull/584)), thanks to [@hamelsmu](https://github.com/hamelsmu)

### Bugs Squashed

- Fix repr issue with `show_doc` ([#588](https://github.com/fastai/nbdev/pull/588)), thanks to [@muellerzr](https://github.com/muellerzr)


## 1.2.0

- upgrade nbconvert dep to v6

## 1.1.23

### Bugs Squashed

- fix verbose flag

## 1.1.20

### New Features

- skip symlinks in recursive glob ([#515](https://github.com/fastai/nbdev/issues/515))


## 1.1.15

### Breaking Changes

- make recursive behavior for `nbdev_build_docs` consistent with `nbdev_build_lib` ([#467](https://github.com/fastai/nbdev/pull/467)), thanks to [@hamelsmu](https://github.com/hamelsmu)

### New Features

- Allow for a one-time only (potentially) .py -> .ipynb generation ([#369](https://github.com/fastai/nbdev/issues/369))

### Bugs Squashed

- Images with `attachment:` break export ([#501](https://github.com/fastai/nbdev/pull/501)), thanks to [@yacchin1205](https://github.com/yacchin1205)
- Docs nav doesn't work on gitlab ([#488](https://github.com/fastai/nbdev/pull/488)), thanks to [@tcapelle](https://github.com/tcapelle)
- clean up all instances of recursive ([#470](https://github.com/fastai/nbdev/pull/470)), thanks to [@hamelsmu](https://github.com/hamelsmu)
- After 'conda install -c fastai nbdev', error "`HTMLExporter` object has no attribute `template_path`" ([#431](https://github.com/fastai/nbdev/issues/431))


## 1.1.13

### New Features

- support windows ([#392](https://github.com/fastai/nbdev/pull/392)), thanks to [@mszhanyi](https://github.com/mszhanyi)
- `nbdev_new`: get template from latest release asset ([#382](https://github.com/fastai/nbdev/pull/382)), thanks to [@hamelsmu](https://github.com/hamelsmu)
- Add more license options

### Bugs Squashed

- Fix recursive flag ([#433](https://github.com/fastai/nbdev/pull/433)), thanks to [@hamelsmu](https://github.com/hamelsmu)
- conda not installing nbdev properly on WSL2 ([#430](https://github.com/fastai/nbdev/issues/430))
- fix nb2md ([#424](https://github.com/fastai/nbdev/pull/424)), thanks to [@hamelsmu](https://github.com/hamelsmu)
- `nbdev_build_lib` seems to convert more notebooks than expected ([#423](https://github.com/fastai/nbdev/issues/423))
- fix default arg issue with `nbdev_update_lib` ([#416](https://github.com/fastai/nbdev/pull/416)), thanks to [@hamelsmu](https://github.com/hamelsmu)
- `nbdev_update_lib` errors out when fname not supplied ([#415](https://github.com/fastai/nbdev/issues/415))
- `nbdev_new` fails on calling the GitHub API without guidance ([#404](https://github.com/fastai/nbdev/issues/404))
- fix recurse issue ([#391](https://github.com/fastai/nbdev/pull/391)), thanks to [@hamelsmu](https://github.com/hamelsmu)
- `nbdev_build_docs`----ModuleNotFoundError: No module named 'fastcore' ([#390](https://github.com/fastai/nbdev/issues/390))
- `nbdev_test_nbs` --fname broke in 1.1.7 ([#388](https://github.com/fastai/nbdev/issues/388))
- set recursive=True for docs ([#387](https://github.com/fastai/nbdev/pull/387)), thanks to [@hamelsmu](https://github.com/hamelsmu)
- fix url for getting branch ([#386](https://github.com/fastai/nbdev/pull/386)), thanks to [@hamelsmu](https://github.com/hamelsmu)
- `nbdev_nb2md` throws error when called in a notebook ([#381](https://github.com/fastai/nbdev/issues/381))


## 1.1.12

### New Features

- `nbdev_new` should grab files from a release asset in `nbdev_template` ([#383](https://github.com/fastai/nbdev/issues/383))
- Use Jekyll Theme instead of vendoring all required files ([#379](https://github.com/fastai/nbdev/issues/379))
- Create relevant directories in `docs/_data` if do not already exist ([#377](https://github.com/fastai/nbdev/issues/377))


## 1.1.6

### New Features

- Clean Google Colab metadata and line endings ([#364](https://github.com/fastai/nbdev/pull/364)), thanks to [@muellerzr](https://github.com/muellerzr)
- add ability to find notebooks recursively ([#359](https://github.com/fastai/nbdev/pull/359)), thanks to [@hamelsmu](https://github.com/hamelsmu)
- Add `bare` flag to `nbdev_build_lib` ([#336](https://github.com/fastai/nbdev/issues/336))
- install git hooks in `nbdev_new` ([#308](https://github.com/fastai/nbdev/issues/308))
- `nbdev_new` now works on an existing cloned repo, instead of creating a new repo ([#307](https://github.com/fastai/nbdev/issues/307))

### Bugs Squashed

- `nbdev_update_lib --fname notebook.ipynb` crashes (while `nbdev_update_lib` works) ([#341](https://github.com/fastai/nbdev/issues/341))
- Copy new files only if they don't exist for nbdev_new ([#309](https://github.com/fastai/nbdev/issues/309))


## 1.1.3

### New Features

- Place source code below heading on #exports ([#265](https://github.com/fastai/nbdev/pull/265)), thanks to [@hamelsmu](https://github.com/hamelsmu)


## 1.1.2

### Bugs Squashed

- update fastcore requirement ([#281](https://github.com/fastai/nbdev/issues/281))


## 1.1.1

### New Features

- Make CLI faster by removing unneeded imports and moving CLI commands to source modules ([#271](https://github.com/fastai/nbdev/issues/271))
- Move `Config` to fastcore ([#280](https://github.com/fastai/nbdev/issues/280))

## 1.1.0
### Breaking Changes

- Remove magics ([#269](https://github.com/fastai/nbdev/issues/269))
- Removed callbacks ([#253](https://github.com/fastai/nbdev/pull/253)), thanks to [@pete88b](https://github.com/pete88b)
- move conda packager to `fastrelease` ([#252](https://github.com/fastai/nbdev/issues/252))

### New Features

- Place source code below heading on #exports ([#265](https://github.com/fastai/nbdev/pull/265)), thanks to [@hamelsmu](https://github.com/hamelsmu)
- always skip cells labeled "skip" in test ([#257](https://github.com/fastai/nbdev/issues/257))

## 1.0.17

### Bugs Squashed

- restrict nbconvert<6 to avoid upgrade problems ([#249](https://github.com/fastai/nbdev/issues/249))

## 1.0.16

### Bugs Squashed

- When generating docs, import cells are run even if not exported ([#248](https://github.com/fastai/nbdev/issues/248))

## 1.0.15

### New Features

- add option to not exec nb for fastpages ([#244](https://github.com/fastai/nbdev/issues/244))
- Enable Codespaces for nbdev ([#243](https://github.com/fastai/nbdev/issues/243))

### Bugs Squashed

- Fix: correct notebook2html path operation for Windows. ([#239](https://github.com/fastai/nbdev/issues/239))

## 1.0.13

### New Features

- remove numpy conda dep and update to fastcore 1.0.5 ([#241](https://github.com/fastai/nbdev/issues/241))

### Bugs Squashed

- allow nbdev imports when not in an nbdev project ([#238](https://github.com/fastai/nbdev/issues/238))

## 1.0.10

### New Features

- Magic flags for tests ([#232](https://github.com/fastai/nbdev/pull/232))
- Add ability to have Colab badges on pages ([#210](https://github.com/fastai/nbdev/pull/210))
- Support for `doc_path` ([#235](https://github.com/fastai/nbdev/pull/235))

### Bugs Squashed

- Remove colab vendor specific tags which cause `nbdev_build_docs` to fail ([#207](https://github.com/fastai/nbdev/pull/207))
- hooks folder inside .git must be manually created before `nbdev_install_git_hooks` ([#230](https://github.com/fastai/nbdev/pull/230))
- updates to how backtick names are converted to doc links ([#218](https://github.com/fastai/nbdev/pull/218))

## Version 1.0.0

- Initial release


