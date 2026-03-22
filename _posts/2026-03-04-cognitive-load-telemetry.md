---
layout: post
title: "Three Lines of Code in Two Weeks — It's Not Always Laziness (or rethinking how we measure developer productivity)"
description: "Time spent doesn't equal cognitive effort and right now we have no way to measure the latter. The hypothesis is: create a lightweight tool that logs iterative activity. Then generate heatmaps or graphs showing where the time actually went and where the moments of peak cognitive load were. From such maps, some kind of unit of cognitive effort could be derived. For example, a graph might show that painting a button cost 10 points, while fixing a bug took 1k."
---

# Three Lines of Code in Two Weeks — It's Not Always Laziness (or rethinking how we measure developer productivity)

I've been thinking about this topic for a long time and finally decided to write it down.

This whole business of evaluating code by the number of lines written, or other attempts to estimate the volume of work, has always bothered me.

I don't write code on an industrial scale now, maybe just some small tools for myself. But I used to write a lot of code and did it for over 15 years.

You'd come to the office in the morning and start writing something, saving along the way, of course. And in the evening, I sometimes liked to hit ctrl+z and watch in fast-forward, even if in reverse order, how the cursor moved, how blocks of code were highlighted, appeared, and disappeared. First, a condition and a loop would appear in one place, then a piece of code from the loop would move into a procedure, the loop would disappear entirely, etc. It's a mesmerizing dance of the cursor and the text beneath it.

<div style="text-align: center;">
  <img src="https://habrastorage.org/getpro/habr/upload_files/c25/5d0/096/c255d00960299d28e500399b5ee8b5c7.gif" alt="Live Coding">
</div>

By the end of the day, a new concise procedure, a couple of insertions into existing blocks. In total, 50-80 lines of code. Often I had to refine legacy code, where you needed to carefully integrate your additions in different places without breaking anything.

And I would ask myself: who saw all these searches and wanderings of mine? To an external observer, only the number of lines in the morning and the number in the evening are visible. But that's not it at all. These 80 lines don't even hint at what I did all day. I'm sure you understand what I'm talking about.

Now, in the era of total fascination with AI, I can't shake the thought that it would be good to legitimize this whole cognitive process.

There won't be instructions on how I did it here. Just a discussion circling the topic.

## Telemetry
On websites, mechanisms for tracking user behavior have long been used. Where they clicked, how long they stayed on the page, how far they scrolled, etc.

Why isn't there something like this in development? Switches between modules, hovering over methods to see tooltips, navigating dependencies, searching, and so on. Typing text, selecting, deleting, moving, adding a library, fixing a config, running.

Making changes, compiling, test runs, reworking followed by recompilation. Step-by-step debugging with stepping in. That's a massive amount of time and cognitive work.

Or debugging an SQL query. You know how it can be, spending a week debugging a heavy query. Looking at plans, measuring I/O statistics, adding indexes. Pulling out pieces of subqueries and debugging them separately, then inserting them back into the main query. Who sees this? No one. Only you.

At the end of the week, your commit looks like 3 short but perfect fixes in the query. What did you do all week? Added those three lines? Sometimes you feel uneasy yourself realizing how your work's result looks to an outside observer.

Everyone is used to evaluating the result, but in development, as in science, 90% of the time is experimentation and error searching. Evaluation tools aren't designed for that. They are designed for the result, as if you're digging a ditch from here until lunchtime.

No one will appreciate all your struggles, trials, and errors, but that's precisely where the result is born.

But if telemetry collected all your actions into a log, and then built a graph from it, or your AI evaluated how difficult it was – for the business, your work would become transparent and demonstrable.

## The Paradox of Mastery
There's a story about Picasso when someone asked him to draw a sketch on a napkin. He did it in a couple of minutes. When asked how much he should be paid, he named a huge sum. The client was outraged – how could you ask for so much for just 2 minutes? To which the artist replied that it didn't take him 2 minutes, but his whole life.

Doesn't this story resonate with developers who spend a massive amount of time on invisible work, and then try to prove to the client that it wasn't just 2 lines of code?

## What If We Tried?
We could collect thousands of honest logs of the development process and logs of imitation, and then train a model on them to identify patterns. Such raw logs, of course, aren't suitable for training a model, but from them, we could build a heat map and/or an activity graph. The graph would show the "pulse" of the process. Someone does it faster, someone slower, but the process would be roughly similar. Your work would become demonstrable. Of course, everything needs to be collected – not just the IDE, but also the environment.

It should be an external utility that simply logs work. In the settings, the user defines what exactly to collect and from which applications. Title filters with regex, object types, and all that. Then it would be visible that you switched from the debugger to some SQL editor (SSMS/PLSQL) or Postman, wrestled with it for a long time, then went to Stack Overflow and scrolled through dozens of pages.

The result would be an incremental record of actions with context, not just the delta of the result. Not for surveillance, but for analyzing how exactly we (humans) do it, because that's the most interesting part.

## Legitimate Laziness or How We Actually Find Solutions
It's well known that a person can't write code from 9 to 6, especially if it requires searching for a solution, not just typing out standard algorithms. Sometimes you just can't think straight. You can force yourself to write all you want – it won't help. You'll write something so messy you won't be able to understand it later. The solution is on the tip of your tongue. You feel it exists and it's quite simple, but a clear picture doesn't form. You've already tried dozens of options, but the perfect result isn't coming together. You need a distraction – read jokes/news, watch cat videos, to let your thoughts defragment. This is incubation, which can last from a few hours to several days. At some point, a flash happens – the solution clicks. You open your code, look at what you've written, and think: my god, what is this?! Delete it! And in 5 minutes, you write a block that works immediately, something that hadn't worked for days before. And that feeling of awkwardness towards yourself: I spent so much time, but if someone asked, there's nothing to show. It's cognitive dissonance. We're used to measuring by volume. If something is worthwhile, there should be a lot of it, right?

How do you explain to the business why you spent one out of two weeks watching videos?

Such a period – incubation-insight – would be visible on a heat map, because it is preceded by a process of intense trial and error, when you rewrote the same piece over and over, then a pause in the IDE, cats in the browser, and a short final solution.

Privacy concerns might arise. But a person can choose what to log and what not to, and it's in their interest. Crucially, the logs don't necessarily have to contain texts; they could contain only markers based on which heat maps can be built. It doesn't matter what exactly was written or what its quality was during the search phase; the number of attempts and the number of options are much more important, because that's where all the time went.

Effective managers might try to use this against you. After all, Petya kept struggling and eventually produced some monstrosity, while Vasya went to watch cats and came back with three lines of perfect code. But this is precisely where statistics on such maps and the impartiality of AI are needed. Similar to how a neural network analyzes fluorography images, when even an experienced specialist sees nothing special, but the neural network sees markers.

Why isn't this available yet?
Well, okay, if someone is dishonest and just faking it, but the majority do their work honestly and love it. When you're engrossed, you don't notice the time flying. You spent the whole day honestly doing something, no cats. But colleagues are already starting to head home. You look at the clock, it's 6 PM. Where's the result? You yourself don't understand where the time went. Such heat maps would help you understand where the moments of maximum tension were and what real intellectual contribution was made, even if there's nothing tangible to show for it.

## Simple Analogy
A school math problem, finding the area of a field, for example.
Problem statement: given A, B, C, what is the area of the field?
You can answer briefly: 1 km².
However, the teacher requires showing the solution, how you got that answer. They want to see the formula. But even that formula is too superficial. It would be more interesting to know an even deeper layer, one that shows the chain of logical reasoning leading to the solution. Where it would be visible why exactly this formula or theorem was applied and what preceded that theorem. Whether it was retrieved from memory as a ready-made recipe, or if you arrived at it yourself. The math example is relevant because you need to derive a formula, but the formula is the result; the process itself remains off-screen. In school, we are taught precisely the process (method) of finding a solution; formulas are just tools.

In school, they teach how to apply the Pythagorean theorem. They drill dozens of problems so that a person approaches the same theorem from different sides. Once the material is absorbed, a new topic begins. But in school, they teach a ready-made process, which over hundreds of years has turned into a manual.

But at work, a person is often forced to build their own process independently. Yes, based on the school one, but independently.
For some, it's more effective, for others less so. And, most likely, the difference in the ability and speed of solving various work tasks lies in the different processes that people have built in their heads. Perhaps a heat map would allow us to understand the difference in this sense between John and Sam. Why Sam solves typical tasks faster than John, but John is capable of solving non-trivial problems where Sam gets stuck.

Maybe these heat maps could find application in science, or perhaps they could replace tests in interviews (instead of solving problems and IQ tests, you could show a "passport" of your thinking style, because that's what everyone is hunting for in hiring, not just knowledge of algorithms)...

Ponder this.

[Originally published on Habr in Russian](https://habr.com/ru/articles/1006222)
