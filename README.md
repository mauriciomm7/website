# TODO List

- [ ] ADD CV download to topbar.
- [ ] UPDATE publication section.
- [ ] CREATE single-bookdown.html /layout/ that contains bookdown that ressembles doc.
- [ ] CREATE single-bookdown.html /layout/ that contains bookdown that ressembles doc.
- [ ] CREATE code snippets (.html or .css) file which can be called for formatting purposes similar to Latex `\commands`
- [ ] ADD Emoticons https://fontawesome.com/v4/get-started/
    - [ ] Mainly for X icon
- [ ] ADD Contact Form: mhttps://github.com/mmistakes/made-mistakes-jekyll/blob/master/src/_pages/contact.md
- [ ] CHANGE publications layout: use colors to visually cue, now too much bold.
- [ ] ADD doi to main website posts:  https://docs.rogue-scholar.org/
- [ ] CREATE Nice teplate with header for blog-posts

- [ ] RESEARCH Website Posts:
	- [ ] Bayesian v Frequentist Theorizing (Think 3B1B)
	- [ ] Logics of Inference in Social Science Research
	- [ ] Collapsability Implications from Higher Level Units (Think of MA) and collapsability.
	- [ ] Combinatorics, Permutations and Combinations
	- [ ] Diff mindsets causal inference and statistical analysis.
- [X] ADD Callouts for creating bookdown sections. 
- [X] FIXED Major bug for deployment
- [X] FIXED Footnote size _stored under utilities_css
- [X] UPDATED publications page.
- [X] ADD Twitter Follow buttom. Decieded not to after ELON takover.

## To execute this website run the following command on the TERMINAL

```Shell
bundle install
gem install bundler
bundle exec jekyll build
bundle exec jekyll serve 
```

## Notes on Development

NTS1: In order for you to have better versioning of workshops/courses taught,  you should create a REPO for each of these and manage iterations with branches. Then, once you have these static websites which can be made of jupyter notebooks, you can hyperlink them to sections on your website. Thus, rather than hosting and version managing courses or workshop files through your website you have greater flexibity and a contairzed env. 

NSF2: When adding sections to the /learn/ component, you should add them using the following settings to ensure a docs like formatting:
```YAML
---
layout: single.html
category: methods 
permalink:
toc: true
toc-location:
title: "Boolean Networks Inference"
---
```

NTS3: Github Actions is broken when running last_update.sh, try changing internal parameters in the function.

```Shell
 - name: Update commit date in HTML files
    run: |
      chmod +x _scripts/last_update.sh
      ./_scripts/last_update.sh
```

 Also, remember to have this <span> element in pages you want it to update:
`<span id="git-last-commit-date"></span>`

NTS4: When  adding custom css snippets that can then be used you should add them directly to the `_custom.css` but alway make sure it is imported to the `_sass\minimal-mistakes.scss` OR `assets\css\main.scss`


NTS5: 
- CHANGE footnote size: _utilities.scss  `.footnote{}` 
- CHANGE website font size and typesetting `_variables.scss` 
- CHANGE main body font size `_base.scss` each category.
- CHANGE navigation font` _navigation.scss` => `.greedy-nav {`