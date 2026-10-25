# Welcome

iCorrVision v2 is a department level project of the [Department of Mechanical and Industrial Engineering](https://www.demi.fct.unl.pt/en) (DEMI) at [NOVA School of Science and Technology](https://www.fct.unl.pt/en) (FCT NOVA). iCorrVision v2, while functional from end to end, needs a lot of polish in order to realise its full potential. In [iCorrVision-2D](https://github.com/iCorrVision/iCorrVision-2D) you will find a modular DIC Python package for 2D surfaces, and in [iCorrVision-Grabber](https://github.com/iCorrVision/iCorrVision-Grabber) you can find the extendable camera acquisition software developed alongside it.

## To all future contributors

Given the development scope of the iCorrVision v2 project as a whole, there is still much to be done and a lot that can be expanded. Feel free to try and make your own changes to it. All levels of contributions are welcome, so don't be afraid of trying it out for yourself. If you come out of the process having learned something, that is more than enough!

### But what if I'm new/don't know how?

There are a lot of resources out there that can help you get a grasp on how things are done in open source projects. GitHub itself has helpful resources explaining the process of [forking and opening a PR](https://docs.github.com/en/get-started/exploring-projects-on-github/contributing-to-a-project). Everyone taking part in the project is expected to follow our [Code of Conduct](https://github.com/iCorrVision/.github/blob/main/CODE_OF_CONDUCT.md), and if you need some pointers on how contributing to open source generally works, [there are resources for that too.](https://opensource.guide/how-to-contribute/)

## Who maintains this?

As of right now the code maintainers of this project are @DanTheRobot (that's me!) and @josexavier3, and eventually more people from DEMI will be added to the project to help out and expand the team. This is also a learning experience on my part when it comes to maintaining and contributing to open source. I will try to review PRs and Issues as they come, but I'm moving on to other projects too, and if those PRs start coming in fast before the team expands you should expect things to slow down a bit. For a general view of how things stand, maintainers are the `@iCorrVision/maintainers` team, and each repository's `.github/CODEOWNERS` file lists which parts need their review.

## What we are looking for

Right now most of the work needed is related to future DEMI level projects, marked as future works as established in my MSc thesis (I will link that document here when I can/am allowed to). However, you are free to make your proposed additions in regards to:

- **New strategy implementations in 2D:** The various strategies implemented in the correlation pipeline, with the exception of the `SubpixelRefinement` class, are easily extendable from their core classes and relatively self-contained. Feel free to make your own issues to add something here! If you want something to look into, I suggest the `PyramidSearch` for example, as it is very underwhelming as it currently stands.
- **New camera backends for the Grabber:** Currently the only proprietary camera backend supported is Allied Vision, so if you need to use a different camera that is an addition you will have to make for now. Although a lot of the code in the camera orchestration layers of the Grabber is currently awaiting important changes, the way camera backends themselves work and are to be added to the Grabber software will hardly differ from what is currently defined in `cameras/template` (if at all).

Work related to the improvement of performance will have to wait as we prepare both applications for a proper release, and although issues related to this will not be ignored, I highly suggest focusing first on more low-risk contributions such as tests.

Lastly, bug reports with real datasets are highly appreciated. As we begin to make iCorrVision v2 a mainstay in the world of DIC software, bug reports offer a look at what the user is currently experiencing that might slip right under our noses as we get accustomed (and to a certain degree desensitized) to the various faults still in the software, be they big or small.

The core files (`engine.py` and `factory.py` in iCorrVision-2D, acquisition orchestration scripts in iCorrVision-Grabber) are where most of the work I want to do is needed. For the correlation, I'm thinking of adding an auto QtForm to add the new strategies to the GUI as well as prepare the engine for future work on performance optimization. The acquisition presenter in the Grabber, on the other hand, is a bit of a mess right now as I coded it mostly while I was still learning about Qt, the MVP design pattern and camera orchestration and syncing, so that needs a bit of a face lift.

In the coming days I will be opening issues for the things I will be focusing on before stepping back a bit from active development of the app.

# Guidelines

## License

Currently, the two repositories under the organization follow the GPL-3.0-or-later license, so keep in mind that *everything **you** commit will follow it too*.

## Before you start

Although there is currently no established hard ruleset on how to go about the issuing for fixes, try to go by the following for now:

- **Strategy subclasses/small fixes:** Code away, just link an issue and I'll check it before merging.
- **Core files:** I would ask you to stay away from those for now, but if you believe you have a very, **very,** ***VERY*** pertinent improvement or change for those, please talk to me ***BEFORE*** coding away.

## Making changes

### Forking

If you read the point above and are now ready to get to work on something, fork and branch with either one of these 3:

- `feat/` for a new strategy or camera backend;
- `fix/` for a bug fix;
- `chore/` for a clean up.

### Committing

**Try to keep one logical change per commit.** If you are like me, when coding for your solo projects you probably have the habit of having giant run off commits that do way too much by themselves, but those tend to be harder to review, so you will be saving us both some time if you remember to respect this one rule.

### Documenting

Currently the project uses Google-style docstrings and black for the styling (plus isort in iCorrVision-2D). Eventually however we might switch to Ruff.

## Testing

Another thing on the TODO list is to write some tests in general. For now: run the example or validation notebook of the area you changed (each repository's README lists them) and say in the PR what you ran (if you are willing to spend your time contributing to such a niche project I will trust you to follow this).

I'll say it again however, a test suite is planned, *soonTM.*

## Pull Requests

Pull requests should follow the same structure as found in iCorrVision/iCorrVision-Grabber#2, meaning:

1. A **summary** of what was done.
2. The **decisions** you, as a contributor and programmer, made for the code.
3. What **tests** you ran to see everything is in order.
4. And if applicable, what **LLM/AI usage** went into the work (see more below on LLM/AI usage in the iCorrVision v2 projects)

Finally, to try and keep some small accountability for the code added, we kindly ask you to tick the checkbox confirming you understand the changes made and submit them under the stated license of the repo.

The pull request template already has these sections and the checkbox. This all sounds a bit scarier than it needs to be, so don't worry too much about it :)

## Review

In the reviewing process you might get asked to explain your code. This is more probable to happen in the case I myself don't understand it, not for you to prove yourself, but still you should be ready to explain it. As I stated before, things might get hectic but I will make my best effort to get back to you as soon as possible with a review.

# LLM/AI Usage

## Why we ask

Keeping personal opinions on LLMs/AI and degrees of usage aside, this check comes not from a place of judgement, but for accountability. As it stands, iCorrVision v2 aims to be/become a student-led project, and if we lose this accountability and understanding of what is going on inside the repos it will eventually lose its purpose.

I myself used quite a bit of LLM/AI tooling to help in writing and learning about the architecture used in this project, and understand how it can sometimes get away from us without intending to, so these rules come as a check on that.

## Disclosure and limits

Everything written by an LLM/AI should be disclosed, that means code, docs, issues, reviews and comments.

Given the fact that these repos will start by following the honor system, we don't really expect you to disclose spellcheck and Q&A processes that involve LLMs/AI, nor just plainly using it as a search engine to parse documentation and learn the libraries and APIs.

***HOWEVER***, please try to draw a limit at decisions made. In 1979, almost 50 years ago as of the time of writing this, a page from an internal IBM training presentation held a singularly important sentence. *A computer can never be held accountable, therefore a computer must never make a management decision*. This is to say: *an LLM/AI cannot take accountability for what you present, therefore the decisions made in the code, *even* if not written directly by you, should be your own.*

## How

Going back to the iCorrVision/iCorrVision-Grabber#2 PR, you can see the ground work for how pull requests with LLM/AI usage should be made:

- **Commits:** `Assisted-by: <Agent>:<model-id>` to determine the exact LLM/AI model used.
- **PR:** An "LLM/AI Usage" section which details the work done by the LLM/AI itself.
- **LLM/AI as an author:** Keeping in mind this is now in the grounds of personal opinion, I believe that if you don't give credit to the keyboard you typed the words with, you should also not credit a tool as if it were a proper contributor, but I won't stop you from having a `Co-authored-by:` line in your commits. However, I do encourage you to turn them off.

## Your responsibility

Although I have already stated this before, you have the responsibility to be able to *explain, defend and fix every line of code you submit*, so I will stress one last time that you should be ready to do so.

