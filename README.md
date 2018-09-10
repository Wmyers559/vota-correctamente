# ¡Vota correctamente!

> *"Hey, wow, FP Coffee is doing a group project again!"*
>
> — You.

This repository is an open-ended programming challenge to the brave men and women in the coffee group. The problem is to implement some sort of voting simulator that can demonstrate the differences between various [electoral systems][1]. Here's the catch: if you wanna get any *street cred* for your solution, you're gonna have to...

## Learn a New Programming Language

The point of this project is to challenge ourselves. You should pick a language that you don't know a lot about, or have little to no experience in. If there's a language you've always been curious to try, but haven't had a good project to start out with, here's your excuse!

Go ahead and let us know how your progress is going, or where you get stuck, so we can talk programming and compare and contrast our solutions as we go.

## Etiquette

Fork this repository to get started. Do all your work in a subdirectory with your name on it. When you're ready to show off, go ahead and merge your solution into the master branch. Oh, and put a README in your project so we can all see what makes your solution so clever.

## The Problem

It's an election year. You need to write a simulation that models a population of voters, who need to elect one out of several candidates to the high office of ***Politician.*** Each voter and candidate has some set of political positions, and the voters need to score the candidates based on how close they feel the candidates' positions are to their own.

You should be able to convert the voters' *feels* into a set of ballots, and score the ballots to pick a winning candidate. However, there's more than one way to score an election.<sup>[[1][2]][[2][3]]</sup> To name a few:

- First Past the Post (boo!)
- Ranked Choice Voting (which has several counting methods):
  - Instant Runoff Voting
  - Borda Counting
  - Condorcet Method
- Approval Voting (which is a special case of...)
- Scored Voting

In your simulation, it should be possible to run the same election multiple times using different voting/counting methods.

All in all, every version of this project should implement these common features:

- Voters and Candidates having different **political positions** on a variety of different (but probably not totally independent) **issues**
- Measuring how far from their ideal each voter thinks a candidate is
- Converting these measurements into **ballots** — FPTP, Ranked, Scored, etc...
- Scoring the election and declaring a winner
- Determining how "happy" the voters are with the outcome of the election

Those are the basic requirements for this *Language Learning Battle Royale!*

Good luck, and happy hacking!

## Stretch Goals

These are just a few suggestions I came up up with that might make this project a little more interesting.

Electoral politics is a hella complicated topic, so there are ***a lot*** more ideas that you could add on to the basic premise of this simulation. These are just the first few things that come to mind for me. If you come up with any other ways to extend this challenge, shout 'em out! This is your time to get creative, yo!

### "Nate Silver" Factor

Add a wonk to the electoral process whose job is to publish statistics which predict each candidates chance of winning. He'll influence voters' voting habits by forcing them to decide between voting **honestly** or **strategically** — given that all the other voters need to do the same.

Bonus points if "should I vote strategically or honestly?" is itself an issue decided by the voter's political position.

### Parliamentary System

What if the population was divided into clusters which each needed to vote for a representative? Instead of electing a single candidate, they would elect a parliament which would *itself* need to vote on political issues in order to steer the ship of state. Are voters happier when executive power is distributed more broadly?

### Tricky Dick Mode

You could try to implement something like corrupt electoral financing, gerrymandering, or some other tactic for voter disenfranchisement. What happens to your elections when the candidates who end up in power can connive and cheat the system to stay in power? Do some electoral systems handle unfair play better than others?

### Quadratic Vote Buying

There's another alternative voting method<sup>[[3][4]]</sup> where people buy votes. The dystopian-ness of this scheme is mitigated (slightly) by the vote pricing strategy: n votes costs `O(n^2)` dollars. You can implement this voting method, where people are willing to pay more to put more votes toward a candidate they like more. Of course, in order to do this you need to distribute a certain amount of expendible wealth among your voting population, which adds a layer of complexity.

Two important things to be conscious of if you want to honestly compare QVB to other voting methods:

1. In the real world, wealth is accumulated according to a [preferential attachment][5] process, which results in wealth following a power-law distribution (by the way, `O(e^x)` >> `O(n^2)`)
2. Personal wealth is not independent from political viewpoint. Wealthier people tend to favor more economically conservative policies.

### Shifting Public Opinions

Allegedly, people sometimes change their minds about what they believe. You could add a random drift to each voter's political positions. Or a system where new generations of voters replace the old. Or one where voters on the fringes feel pressure to conform to the their group's positions.

One thing that would be really interesting is if voters changed their opinions in response to a candidate's term in office. Maybe if her term goes well it will serve to normalize her more fringe political positions. Or if she presides over dark times, maybe she'll alienate people from her more centrist points of view.

This would be way more complicated because you wouldn't just need to model *beliefs* about what *should happen,* but how voters respond to the changes that take place when candidates make decisions that change the world they live in.

### The Spectacle

What if there are discrepencies between what voters **think** a candidate's positions are vs. the **actual consequences** of electing that candidate? Introducing errors into the process voters use to compare the candidates' positions to their own complicates the situation. Determining the how "happy" a voter is with a candidate's term becomes more difficult than of figuring out who she'd be most likely to vote for.

A particularly snarky way to do this might be to have certain issues that are not-up-for-debate, (either because they are hidden from view or universally agreed upon by all candidates), but still have that issue effect how "happy" the voters are with the candidate's term. Conversely, you could add "fake issues" to the election that don't impact anyone's lives, but still get used by voters in deciding how to vote.

<hr/>

P.S.

Just wanted to remind you that by writing your own rules to simulate a person's opinions, desires, and general happiness with the world they live in, you're inevitably making some sort of opinionated statement that tells everyone your personal views on human nature...

No pressure tho! :)

[1]: https://en.wikipedia.org/wiki/Electoral_system
[2]: https://ncase.me/ballot/
[3]: http://zesty.ca/voting/sim/
[4]: https://corpgov.law.harvard.edu/2013/06/06/quadratic-vote-buying-square-root-voting-and-corporate-governance/
[5]: https://en.wikipedia.org/wiki/Preferential_attachment
