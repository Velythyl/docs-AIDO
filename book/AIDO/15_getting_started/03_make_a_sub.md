# Make your first submission {#cm-first status=ready}

This section describes the steps to make your first submission.

## Checkout the submission repo {#cm-first-checkout}

Check out the competition template [`hallenge-aido_LF-template-random`][template]:

    $ git clone -b daffy https://github.com/duckietown/challenge-aido_LF-template-random

[template]: https://github.com/duckietown/challenge-aido_LF-template-random

## Submit {#cm-first-submit}

Jump into the directory:

    $ cd challenge-aido_LF-template-random

Submit using:

    $ dts challenges submit --challenge aido5-LF-sim-validation

What this does is:

1. Build a Docker container.
2. Push the Docker container.
3. Make contact with the [challenge server][server] to send your submission.

[server]: https://challenges.duckietown.org/v4/

The expected output is something along the lines of:

    Sending build context to Docker daemon  5.632kB
    ...
    ...
    Successfully created submission 23
    
    You can track the progress at: https://challenges.duckietown.org/v4/humans/submissions/NNN
    
    You can also use the command:
    
       dts challenges follow --submission NNN

where `NNN` is your submission id.

## Monitor the submission {#cm-first-monitor}

There are 2 ways to monitor the submission:

The first way is to use the web interface, at the URL indicated.

The second way is to use the `dts challenges follow` command:

     $ dts challenges follow --submission ![submission ID]

## Look at the leaderboard {#cm-first-leaderboard}

The leaderboard for this challenge is available at the URL

> [`https://challenges-stage.duckietown.org/humans/challenges/aido5-LF-sim-validation/leaderboard`][leaderboard]


[leaderboard]: https://challenges-stage.duckietown.org/humans/challenges/aido5-LF-sim-validation/leaderboard

In general all of the challenge leader boards can be viewed at the front page [the challenges website][challenges].

[challenges]: https://challenges.duckietown.org/v4/



## Local evaluation {#cm-local}

You can also evaluate the submission *locally*.  This is useful for debugging and development.

Use this command:

    $ dts challenges evaluate  --challenge aido5-LF-sim-validation

### Troubleshooting

If any of the commands above don't work, it is likely that something related to Docker permissions is to blame - please file an issue, as we are trying to fix that problem.

<!-- TODO: where to file an issue? -->