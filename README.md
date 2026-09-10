# COSC 407 / 507 — Lab 0: get a working toolchain

**Do this in the week of 14 September, before your Lab 1 session.**

Lab 0 is marked for **completion only**. It exists so that you never spend Lab 1
installing a compiler. Every later lab is done and submitted inside the two-hour
lab period, and there is no time in that period to fix a broken environment.

**You may use AI freely for this lab**, including for installation problems. The
no-AI rule that starts in Lab 1 is about the concurrency code you write, not
about making a container start.

## Pick one of these three. The first is easiest.

### 1. GitHub Codespaces — nothing to install

First, get your own copy of this repo.

Go to github.com/cosc407/lab0 and click the green "Use this template" button, then "Create a new repository."
Name it something like lab0-\<your-username\>. Choose Private so your submission isn't visible to classmates.
This creates your own separate copy — you now own it and can push to it freely. There is no ongoing link back to cosc407/lab0.

Then open it in Codespaces. Open your new repository on github.com, then Code → Codespaces → Create codespace on main. Wait a couple of minutes for the container to build the first time. You get VS Code in your browser with the whole toolchain ready.

Works on Windows, macOS and Chromebooks. As a verified student you get 180 Codespaces core-hours a month free with the Student Developer Pack. Stop your codespace when you finish — it bills by wall-clock time, not by whether you are typing.

### 2. Docker or Podman on your own laptop

Install Docker Desktop (free for enrolled students) or Podman Desktop, plus VS
Code with the **Dev Containers** extension. Clone this repository, open it in VS
Code, and accept "Reopen in Container".

On an Apple Silicon Mac, make sure you are running the arm64 image and not amd64
under emulation — emulated timings are not comparable to anything, which matters
in a course about measuring speed.

### 3. An SCI 234 lab machine

Use these if you have no laptop. Check with your TA in Lab 0 week that the
toolchain is present on them — do not assume it.

## Then run this

```sh
make
./baseline 10000000 5
make test
```

`make test` checks that gcc, make and pthreads all work, and that you have
filled in `RESULTS.md`. If it fails, sort it out **this week**, on the course
forum (Canvas Discussions) if necessary.

## What you actually do

`src/baseline.c` is written for you — you do not write any C in Lab 0. It sums
1…n on one thread several times and reports how much the timing varied between
runs of *identical* work.

That spread is the whole point. From Lab 1 onward you will be claiming that one
version of a program is faster than another. Such a claim means nothing until
you know how much your own machine wobbles when nothing has changed at all. Find
out now.

Fill in `RESULTS.md`, commit, and push:

```sh
git add -A
git commit -m "Lab 0"
git push
```
