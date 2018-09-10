# ¡Vota correctamente!

> *"Hey, wow, FP Coffee is doing a group project again!"*
>
> — You.

This repository is an open-ended programming challenge to the brave men and women in the coffee group. The problem is to implement some sort of voting simulator that can demonstrate the differences between various [electoral systems][1]. The only rule is, if you wanna get any **street cred** for your solution, you're gonna have to **learn a new programming language!**

Challenge yourself! Pick a language you don't know a lot about, or have always been curious to try, and start from scratch in that language. Let everyone know when you make progress, or get stuck, so we can discuss and compare and contrast as we go!

## The Simulation

It's an election year. Your simulation needs model a population of voters, who need to elect a one out of several candidates to the high office of ***Politician.*** Each voter and candidate has some set of political positions, and the voters need to score the candidates based on how close they feel the candidates' positions are to their own.

You should be able to convert the voters' *feels* into a set of ballots, and score the ballots to pick a winning candidate. However, there's more than one way to score an election.<sup>[[1][2]][[2][3]]</sup> To name a few:

- First Past the Post (boo!)
- Ranked Choice Voting (which has several counting methods):
  - Instant Runoff Voting
  - Borda Counting
  - Condorcet Method
- Approval Voting (which is a special case of...)
- Scored Voting

In your simulation, it should be possible to run the same election multiple times using different voting/counting methods.

All in all, every version of this project shoule implement these common features:

- Voters and Candidates having different **political positions** on a variety of different (but probably not totally independent) **issues**
- Measuring how far from their ideal each voter thinks a candidate is
- Converting these measurements into **ballots** — FPTP, Ranked, Scored, etc...
- Scoring the election and declaring a winner
- Determining how "happy" the voters are with the outcome of the election

Some interesting stretch goals that you might want to consider:

- Adding a "Nate Silver" factor to the election, wherein a data wonk is publishing statistics which predict the candidates' chances of winning
  - Under this system, voters may need to decide whether they are going to vote **honestly** or **strategically** in order to get the candidate they want
  - Bonus points if "should I vote strategically or honestly?" is itself an issue decided by the voter's political position
- Shifting public opinions in response to a candidate's term in office
  - Maybe if her term goes well it will serve to normalize her more fringe positions; or if she presides over dark times, maybe she'll alienate people from her more centrist ones
- Having discrepencies between what voters **think** a candidate's positions are vs. what they actually are
  - If what you see is not what you get, then figuring out how "happy" a voter is with a candidate's term can be a bit trickier than measuring who she'd be most likely want to vote for.
- Implement corrupt electoral financing, gerrymandering, or some other tactic for voter disenfranchisement, so that candidates who end up in power can connive and cheat the system to stay in power. Do some electoral systems handle unfair play better than others?
- Whatever else you can think of! Get creative, yo!

<hr/>

P.S.

Just wanted to remind you that by trying to simulate people's opinions, desires, and general happiness with the world they live in, you're inevitably going to have to make some opinionated claims concerning your personal views on human nature...

No pressure tho! :)

[1]: https://en.wikipedia.org/wiki/Electoral_system
[2]: https://ncase.me/ballot/
[3]: http://zesty.ca/voting/sim/
