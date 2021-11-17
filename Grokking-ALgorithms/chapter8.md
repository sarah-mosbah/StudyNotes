# Greedy Algorithm

### Intro:
- Greedy Algorithm is about the easiest first solution.
- it doesnt care about the most optimal solution but the first easiest one.


## Approximation algorithms:

### **problem:**
Suppose you’re starting a radio show. You want to
reach listeners in all 50 states. You have to decide what
stations to play on to reach all those listeners. It costs
money to be on each station, so you’re trying to minimize the
number of stations you play on. You have a list of stations.
Each station covers a region, and
there’s overlap.
How do you figure out the smallest set of
stations you can play on to cover all 50
states? Sounds easy, doesn’t it? Turns out
it’s extremely hard. Here’s how to do it:


1. Pick the station that covers the most states that haven’t been covered
yet. It’s OK if the station covers some states that have been covered
already.
2. Repeat until all the states are covered.
This is called an approximation algorithm. When calculating the exact
solution will take too much time, an approximation algorithm will
work. Approximation algorithms are judged by
• How fast they are
• How close they are to the optimal solution
Greedy algorithms are a good choice because not only are they simple
to come up with, but that simplicity means they usually run fast, too.
In this case, the greedy algorithm runs in O(n^2) time, where n is the
number of radio stations.