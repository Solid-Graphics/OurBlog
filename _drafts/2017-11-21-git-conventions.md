---
layout: default
title:  "Git Conventions"
categories: main
---

Good branch naming in git:
1º Short and forthcoming names (ex:"new-view") 
and use always when possible lowercase names, as urls are by norm are also lowercase

2º Each word separated by hifen

3º If the branch is needed for something external
like an issue, feature, bug, etc, make that the name followed by a identifier

4º If the branch is to be used by more than 1 person
use the name followed by a person identifier (Ex: feature-1234/ms)


Good commit naming in git:
1º	Each LOGICAL change should be its own commit, even if large.
	You can add 300 url fixes to a file and submit that as one commit,
	but if you make 1 url change and a file delete,
	that automatically promotes the second to its own commit.
	
2º  Commit early and often so rollbacks are easier to manage

3º	Commits should be posted in order of execution and dependency.
	A commit for a child feature/issue/update/etc should not be posted
	before the parent one if its dependent on it
	
4º	You can use an unpushed branch as a store for commits as snapshots.
	Even so, use the all the previous points as reference
	
	Messages
5º	Avoid using the terminal to post commits since it incites bad practices

6º	The first line of each commit should be descriptive yet succinct,
	and preferbally not longer than 50 chars, capitalized
	and written in imperative present tense (like explaining what the code
	does when reaching that stop of the commit)
	
	Follows a blank line, followed by a wrapped extended description,
	up to 72 chars per line, explaining the why, how and what could happen.
	
	The description should have pointers if needed (links, refs, etc).
	It should also be intemporal, capable of being understood at anytime.
	
	any commit dependencies must be referenced A -> B

7º	When squashing commits, use --squash and --fixup to make your intents clear
	Use --autosquash for rebasing 
	
Good Merging practices:
1º	DO NOT REWRITE PUBLISHED HISTORY, EVER (Even more if is an importante branch)
	Extreme exceptions
		a) non reviewable and single use branch
		b) clean up

2º	Keep history clean and simple, make sure to:
	a) keep it in accord to what was previously defined
	b) rebase to parent branch (será que isto evitava a cena do código externo dos pull requests?) (R: aparentemente sim, falar com o antunes)
	
3º	Avoid fast forward if you have more than a single commit on your branch

Misc:
1º Chose a method and stick with it, be consistant!
2º Don't push bad or unfinished code
3º Tag your code if needed, a do prefer light ones
4º run git-gc to cleanup, git-prune to snip unreachable objects
	and git-fsck to do consistency checks