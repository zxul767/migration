---
description: The origins of my interest in AI
---

# Prelude

## The Seeds of a Quest

I became interested in Artificial Intelligence (AI) as a teenager, inspired by science fiction movies (e.g., The Matrix, I Robot) that ignited my imagination with a burning question: “Is it really possible to create artificial intelligence?” 

Even back then, without almost no knowledge about AI or Machine Learning (ML), I had an innate intuition that there should be a way to do it, that it wasn’t some impossible task like time travel. But the fact that scientists seemed to have made so little progress after about 50 years since modern computers were created was quite intriguing: “Reverse-engineering the brain must be much harder than reverse-engineering the heart or any of the other organs whose nature doctors know very well these days”, I thought.

After a couple of years in college, where I became fascinated with algorithms and computation, thoughts concerning AI once again arose in my head during my senior year. Many years earlier I had become obsessed with chess, and although I didn’t play actively anymore, I thought that creating an AI to play chess (a chess engine, as they are called) would be a very interesting challenge for my undergraduate thesis. It would combine an old hobby of mine, knowledge about computation and algorithms, and some research on the artificial intelligence techniques that had allowed IBM’s Deep Blue to defeat the world’s former champion (Gary Kasparov) just a few years earlier.

Much like it must have been for the characters in the Wizard of Oz, my discovery of “what lies behind the curtain” was a bit of a disappointment. Misled by science fiction, I was expecting something far more perplexing behind chess engines. Instead, I found recursive search, minimax, and a few other computational techniques. Not trivial stuff, to be sure, but all well within the realm of what I considered classical computer science.

{% hint style="info" %}
The code in this snippet is one of the few basic building blocks in most chess engines. Now, don't get me wrong, there are obviously many more details in a real implementation (and part of the reason why it took me so long to complete one myself from scratch), but this truly represents one of the fundamental ideas.
{% endhint %}

```python
def negamax(node, depth, color):
    if depth == 0 or is_terminal(node):
        return color * evaluate_statically(node)
    value = −∞
    for child in node:
        value = max(value, negamax(child, depth − 1, −color))
    return −value
```

To be fair, I was initially quite surprised that such relatively simple techniques could in fact produce a chess engine that was sophisticated enough to be a challenging and fun opponent (for an amateur player as myself, anyway). I vividly remember the deep satisfaction I felt when I played the first complete game and I didn’t feel like I was playing against a complete novice. Perhaps a big part of that satisfaction came from the idea that I had created an “intelligent” program.

But a crucial element of any intelligent system was missing: the ability to learn. So I decided to expand the scope of the project to incorporate that. My thesis partner and I affectionately called it MAE, an acronym for _Motor de Ajedrez Evolutivo_ in Spanish (or Evolutionary Chess Engine), reflecting the idea that our research would focus on how to evolve its playing skills over time. 

At that point, I had no idea whether imbuing a program with any kind of learning capabilities would be feasible, but it seemed like an interesting challenge for an undergraduate thesis. After a bit of research I found out about Arthur Samuel’s checkers program (back in the 1960s), which had managed to learn from its own games and eventually defeat its creator. So I figured we would be able to, at the very least, replicate for chess what Samuel did in the domain of checkers.

A few months into the project, I realized we had perhaps gotten ourselves into something too ambitious for the amount of time we had available (about a year). I was reading as much as I could about chess engines, classical AI techniques, and some theories of learning, but soon I realized that just getting a fast and robust implementation of the chess engine was more difficult than I initially expected (and the requirement that it be fast was something we couldn't just dodge since the type of learning we ended up using required enormous amounts of self-play). After about 6 months, we had a working engine, and it was now time to incorporate learning capabilities into it.

And that’s when we hit a wall. I realized that although there was some literature about learning, there wasn’t anything that we could just implement and make work in a short time. We would need to do some serious research and possibly try many things, get into one or more dead ends, backtrack, and perhaps eventually stumble upon something that actually worked as I envisioned. Lots of fun, yay! Except we only had less than 6 months left. Ouch!

That’s also when I first realized that despite all the fuss that Deep Blue had caused at the time, it was far from being an intelligent program, as it also lacked any ability to learn. All of its strength in playing chess came from hard-coded domain knowledge and quasi brute-force search into the space of possibilities.

In the end, we added some crude form of learning into the engine by having it evolve an evaluation function (an important part of what determines its playing strength) using genetic algorithms during a training phase "offline". Learning about that and implementing it was fun and actually resulted in a noticeable improvement over our initial intuitive tuning of the evaluation function, but somehow I still thought there was something missing and I felt unsatisfied. 

At the beginning of the project, I had envisioned a program that would learn more like we humans do: “online” and continuously as it played more and more games. I had read a bit about reinforcement learning at the time and I felt it was a promising path, but our time constraints didn’t allow me to get deep enough into it to attempt an implementation.

## **The Quest Begins**

After I graduated, I went on to work on software engineering due to personal circumstances, but it always remained in the back of my mind to one day go back to exploring the fascinating idea of how to build intelligent machines.

Many years later, I started to hear in software engineering circles more and more about ML and AI. I didn’t know it at the time, but quite a few researchers had just started to make some breakthroughs in the field of ML (particularly in computer vision), showing that the connectionist approach (started as early as 1960, but ignored for the most part during decades) had been unjustly underestimated in the past. Once again, I started getting interested and learned more about modern ML. This time, some of the applications I saw (e.g., somewhat robust handwritten character recognition) made me feel like there were interesting developments that definitely went beyond the classical techniques I had seen back in college.

Over the following years, as my knowledge in Machine Learning—and Deep Learning in particular—became deeper, I started to think about the source of its limitations, and more broadly about intelligence. I read “I Am a Strange Loop” and “Gödel, Escher, Bach” by D. Hofstadter and they both inspired me to think even more deeply about the nature of the ultimate problem that everyone working in AI/ML was facing. While not everyone doing research in AI/ML was deeply concerned about figuring out general mechanisms for intelligence (some were content with discovering mechanisms to solve more narrow problems), I felt that it was the most efficient springboard to solving many other problems humanity faced, and that if I was going to put so much energy and time into something, it might as well be an ambitious problem, however difficult it seemed to many at the time.

From foundational courses in ML/DL, I was well aware that the models used (various flavors of neural networks) were just roughly inspired on actual neuroscience, so intuitively I wasn’t too surprised about the limitations (I imagined that it wasn’t plausible that whatever mechanism the brain uses had been reverse-engineered so quickly), but I got curious about the underlying reasons why such models were very successful for some tasks (e.g., recognizing an arbitrary dog in a picture after having been shown hundreds or thousands of similar pictures), while a complete failure in others (e.g., recognizing that a cartoon of a dog represents the same concept as a photograph of a dog; namely, the failure to “see” abstractions of objects.)

While I was pondering some of these thoughts, a myriad of questions such as “What are really thoughts in our head?”, “What is consciousness?”, “Where does our ability for abstract thinking come from?”, threw me into what I knew would be a lifetime research into the nature of thoughts, minds and intelligence.

Fortunately for me, I am not the only person thinking about this. While it is the case that most research in AI/ML has focused on DL in the last decade (and deservedly so, after proving its value in advancing the state of the art in many application domains), there have been and there still are several other people whose line of research has focused on trying to create more general theories of intelligence, pondering questions that are in the frontier between Philosophy of Mind and Artificial Intelligence. 

That DL is not likely to be the final answer to the intelligence puzzle is something that few top researchers dispute these days. Some of the most prominent in the field admit that we may be starting to reach diminishing returns, and that it’s time to expand the frontiers by reflecting on what we’ve learned, and then start exploring all the other problems that DL has not been able to address so far.

The present essay is therefore a reservoir of my ongoing research, which includes the compilation of various ideas and theories on thinking, minds and intelligence; the analysis of their merits, their intersections, their points of disagreement, and their connections to other relevant disciplines (including but not limited to neuroscience, complex systems, semiotics, and philosophy of mind.), as well as my own reflections and ideas on those topics.\
