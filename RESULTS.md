# Lab 0 results

Name:  Kithe Kisia
Student number:  31181217
Lab section:  L03 Tuesday Morning

## Which environment did you use?

Tick one, and say how many cores it reported:

- [x] GitHub Codespaces — cores:
- [ ] Docker or Podman on my own laptop — OS and cores
- [ ] An SCI 234 lab machine — cores
- [ ] Something else — describe it

## Tools and sources

Tools and sources: I attempted to use the workspace AI for an explanation but it was no help

> Required on every lab. For Lab 0 you **may** use AI to help with installation
> and setup problems — just say so here, e.g. "used Claude to work out why Docker
> Desktop would not start on Windows 11". From Lab 1 onward the restriction
> applies to the code you write, never to the toolchain.

## Two baseline runs

Run it twice, with a gap of a minute or two, and paste both:

```
gcc -std=gnu11 -O2 -Wall -Wextra -Iinclude -pthread -o baseline src/baseline.c
n = 10000000, 5 repeats
  run 0: 0.004487 s
  run 1: 0.004867 s
  run 2: 0.004707 s
  run 3: 0.005156 s
  run 4: 0.004271 s
best  0.004271 s
worst 0.005156 s
mean  0.004698 s
spread 20.7% of best
```

```
make: Nothing to be done for 'all'.
n = 10000000, 5 repeats
  run 0: 0.004787 s
  run 1: 0.006923 s
  run 2: 0.007442 s
  run 3: 0.005610 s
  run 4: 0.005047 s
best  0.004787 s
worst 0.007442 s
mean  0.005962 s
spread 55.5% of best
```

## What you noticed

**0.1** What spread did you get between the fastest and slowest run of
*identical* work? Give the percentage.
I saw a percentage change of the 5 reapeats with the slowest run coming in the second half

For the first I got 20.7%
For the second I got 55.5%

**0.2** Suppose in Lab 4 you measure a parallel version and it comes out 4%
faster than the serial one. Based on your spread above, would you believe it?
One sentence.

Yes I would beleive it as ive seen a change of over double int he eprcentage

**0.3** Anything that went wrong during setup, and what fixed it. One or two
lines — this genuinely helps us fix the instructions for next year.

I think the time in between the runs can be a little clearer, like an exact time for conistency of results

On colab I spent a good bit of time before running the results again, and the results showed a diffrent variation compared to this one.