# Git Usage Guide - How to use it effectively
===============
This guide is intended for those of you who already know how to use Git and are, probably, already familiar with using Git as a source code repository for your own codebases.

If you don't know how to Git yet, try School of Code's course to get you started:
https://www.codeschool.com/courses/try-git

## Collaboration
No matter how you try to dice it up, a code project always has a minimum of two developers - you, and yourself when you wrote that commit two weeks ago! Thus, while these guidelines are going to highlight things to do that are more important when you have multiple developers working on the project together, some of them will be applicable to you even if you work completely alone.

### Commit Messages
There are any number of guides out there describing the best way to write a commit message. Over the years, the Git community has pretty well settled on a few variations around Linus's (the dude that created Git) recommendations. I'll give you a summary as follows:

- The first line of a Git commit should probably be less than 50 characters long and be an overall summary of the commit. Some people accept first lines up to 78 characters, but try not to go over this as it will cause problems with a lot of Git tools out there.
- The first line should be in present tense! That means that, instead of "Fixing an issue with the form dropdown", you should use "Fix an issue with the form dropdown" (My example is vague. Your commit messages should not be however)
- After the first line (I tend to skip a line, but many people don't bother to skip), describe your commit in more detail if it is needed. Avoid discussing the code (everyone can see it anyway by looking at the patch). What you want to put here is your description of the problems you ran into, the reasoning for the choices you made, and any notes about possible problems or future considerations. Remember that having a long message here might be a code smell that your code architecture or solution has some problems that you might need to address
- Subsequent lines can be longer than the first, but try and keep it below 78 characters when possible.

Example:

```
Fix an issue with the form dropdown
- The form dropdown now correctly transitions from closed to open
```

Some projects will have their own commit formatting rules. Check the project's README.md file for instructions on how to contribute. Some projects will reject commits with bad formatting, so be conscious of that!

### Pull Requests
Since WildStarNASA publishes its Git Repositories through Github, I will be basing everything on the assumption that you are also using Github.

#### How to make pull requests:
https://github.com/kirillian/git_usage_guide/blob/master/how_to_pull_requests.md

#### Managing pull requests as a repository maintainer:
So, by now, you've received a pull request from an excited and helpful developer who wants to contribute to your project. What do you do about it and how do you deal with it? The first thing to do is look over the commit. When you are on the page with the pull request, decide if the commit(s) is(are) good or if the pull request needs some work. Sometimes there are formatting problems that you want to be fixed before you let something into the codebase. Sometimes, the feature or bug is something that you don't even want in the codebase at all.

If it's a great commit, the process is fairly easy. There is a button that says 'Merge pull request' that you can use to accept the pull request and merge the code into your repository. If you want the developer to do a little more work before it's ready, the discussion page is the right place to do that! Let the developer know what you want and why. Often the developer will be more than willing to accomodate you and fix the issue!

If the commit requires a lot of work, let the developer know that too. There may be times where the pull request is something that you want and the developer either seems unable to fix the request themselves, unwilling, or they abandoned it entirely. In these cases, you may want to fix the problem yourself before accepting a merge request. Github can help you out here too! There's a small link below that merge button that says 'command line'. Click on that link and Github will provide you with some instructions for how to pull that merge request onto your own local machine and test it out and maybe even fix it up!

There are also, sadly, times when a developer wants to add a feature to your codebase that you don't feel fits within your vision. It's ok to say no! However, being polite is the best way to do so without discouraging others from coming back to help you in the future on other things.
