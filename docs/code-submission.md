# Soccer Sim Code submission

To take part in the Soccer Sim challenge, the code that's powering the team's
robots needs to get to the organizers.

Let's talk a bit about how to do this.

## Too long; Didn't read (TL;DR)

We expect you to submit the code of the `rcj_soccer_team_blue` controller.

Simply add a `team_name.txt` file to the `controllers/` directory and then
zip it together (by creating a `.ZIP` file) with the `rcj_soccer_team_blue/`
folder. That gives you a submission package which you can then share with the
organizers.

A more in-dept tutorial can be found below.

## From controllers to a submission

Suppose you have the folder structure which looks like this

```
controllers/
├── rcj_soccer_team_blue/
│   └── rcj_soccer_team_blue.py
│   └── robot1.py
│   └── robot2.py
│   └── robot3.py
|   └── utils.py
```

To submit it for the competition, there are two (well, maybe three) things we
need to do:
1. Add a team name
2. (Optionally) add a team logo
3. Create a ZIP archive

### Add a team name

The folder structure above does contain some code but it is not immediately
obvious which team does it belong to.

To make it obvious, please create a file called `team_name.txt` on the same
level as `rcj_soccer_team_blue/`. This file should contain a single
line of text: the name of the team (up to 32 characters).

The resulting folder structure would then look as follows:

```
controllers/
├── rcj_soccer_team_blue/
│   └── rcj_soccer_team_blue.py
│   └── robot1.py
│   └── robot2.py
│   └── robot3.py
|   └── utils.py
└── team_name.txt
```

### (Optionally) add a team logo

**Note:** _This step is completely optional and you can just skip it -- your
robot controllers will still work, even if you do not provide a custom logo for
your team_.

If you'd like, you can optionally also add a custom logo for your team's
robot. It will be used as an overlay on the robots in the simulator.

The logo needs to be stored in the [PNG format](https://en.wikipedia.org/wiki/Portable_Network_Graphics)
and located in a file called `logo.png`.

If you choose to add one, the folder structure will look something like the
following:

```
controllers/
├── rcj_soccer_team_blue/
│   └── rcj_soccer_team_blue.py
│   └── robot1.py
│   └── robot2.py
│   └── robot3.py
|   └── utils.py
├── logo.png
└── team_name.txt
```

### Create a ZIP archive

This step is very simple: you just pick **the directory** that contains
the code for your three robots, the `team_name.txt` file and optionally `logo.png` and put them all
together into a single `.ZIP` file. There are many utilities that will do the
job -- we can recommend [7-Zip](https://www.7-zip.org/).

When you look into the resulting `.ZIP` file, the folder structure should look
as follows:

```
.
├── rcj_soccer_team_blue/
│   └── rcj_soccer_team_blue.py
│   └── robot1.py
│   └── robot2.py
│   └── robot3.py
|   └── utils.py
├── logo.png
└── team_name.txt
```

Note that there is no `controllers/` folder anymore -- the `.ZIP` file only
contains a single `rcj_soccer_team_blue/` folder and a single text file called
`team_name.txt` (and optionally the `logo.png` image).

## Uploading your submission

Once you have your `.ZIP` file ready, the only thing left is to submit it to
the organizers. In practice, this generally means uploading it to a specific
location that will be shared with all the participating teams well before the
submission deadline.

## Things to keep in mind

- The resulting `.ZIP` file can be at most 10MB in size.

- The organizers will run a code similarity detector on the submitted code.
    Yes, wheels really do not need to be reinvented but it would really not be
    fair to win a competition with something that's not primarily the team's
    own work. Submissions with significant overlap of duplicated code will not
    be permitted to compete in the competition.

- The code you submit will be open sourced at the end of the competition.

- If you managed to find a bug, have any question or ran into some problem,
    please do not hesitate to ask [on the forum](https://junior.forum.robocup.org/c/robocupjunior-soccer/5).
