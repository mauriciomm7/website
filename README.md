# TODO List
- [ ] UPDATE publication section. 
- [ ] CREATE single-bookdown.html /layout/ that contains bookdown that ressembles doc.  	
- [ ] ADD Twitter Follow buttom
- [ ] CREATE code snippets file which can be called for formatting purposes similar to Latex `\commands`
- [ ] ADD Emoticons https://fontawesome.com/v4/get-started/


- [ ] RESEARCH Website Posts:
	-	[ ] Bayesian v Frequentist Theorizing (Think 3B1B)
 -	[ ] Logics of Inference in Social Science Research
	-	[ ] Implications from Higher Level Units (Think of MA)
	-	[ ] Combinatorics, Permutations and Combinations
	-	[ ] Diff mindsets causal inference and statistical analysis.
  
- [X] FIXED Major bug for deployment
- [X] FIXED Footnote size _stored under utilities_css

## To execute this website run the following command on the TERMINAL

```
bundle install
gem install bundler
bundle exec jekyll build
bundle exec jekyll serve 
```


## Notes on Development 
NTS1: In order for you to have better versioning of workshops/courses taught,  you should create a REPO for each of these and manage iterations with branches. Then, once you have these static websites which can be made of jupyter notebooks, you can hyperlink them to sections on your website. Thus, rather than hosting and version managing courses or workshop files through your website you have greater flexibity and a contairzed env. 

NSF2: When adding sections to the /learn/ component, you should add them using the following settings to ensure a docs like formatting:
```
---
layout: single.html
category: methods 
permalink:
toc: true
toc-location:
title: "Boolean Networks Inference"
---
```