---
description: What do we mean by "understand"?
---

# On Understanding

## Key Ideas

{% hint style="info" %}
To "understand" is a ubiquitous term but its precise definition is often elusive. To have productive conversations in AI/ML and related disciplines, it is important to try to define it as precisely as possible.
{% endhint %}

{% hint style="info" %}
One provisional definition is: "to understand something" means "to be able to predict its behavior and properties in one or more contexts". This may happen through a combination of analogy-making and learning of predictive models at one or more levels of abstraction, in one or more contexts.
{% endhint %}

{% hint style="info" %}
Understanding lies on a continuum, but it's possible to draw arbitrary fuzzy lines to differentiate betweens major levels (e.g., human-level understanding vs. dog-level understanding).
{% endhint %}

## A Ubiquitous but Elusive Concept

Every time a new ML model improves the state of the art on some task (e.g., computer vision, question answering, etc.),  someone will invariably point out (often in a dismissive tone) that it's a nice result but it has no real "understanding" as we humans do.

While the term may seem very intuitive to most people, not everyone can immediately tell you what it really means to "understand" something. And while an intuitive understanding of the term (no pun intended) is enough in casual conversation, we need to pin down with more precision what we mean by it if we want to have productive analyses of intelligence in the context of AI and ML.

{% hint style="warning" %}
Failing to define this important term is often the cause of much philosophical unproductive debate. [The Chinese Room](https://plato.stanford.edu/entries/chinese-room/) argument, by philosopher John Searl, is one classic example of this phenomenon. He denies the possibility that systems can be created that "understand" like humans do, but he fails to provide a clear definition of what he means by the term when presenting his argument. That seems to me like a non-starter for any serious conversation, philosophical or otherwise.
{% endhint %}

## Understanding as Prediction

In his book “On Intelligence”, J. Hawkins regards the ability to predict as the basis for cognition. He concludes that "understanding" is essentially the ability to predict. Stated as is, the rebuttal comes easily when we look at current DL models: they are able to make very accurate predictions for test benchmarks, but upon more careful examination (e.g., when analyzing [adversarial attacks](https://towardsdatascience.com/breaking-neural-networks-with-adversarial-attacks-f4290a9a45aa) on CNNs) we realize that their "understanding" is not what we intuitively consider to be "true understanding". In particular, their inability to abstract beyond the probability distribution of their training set, and their complete inability to build causality models of the world, is perhaps what is often most criticized as lack of "true understanding". 

It is interesting to do some introspection on this, because like many other things we learn implicitly about the world, it is not always so easy to map the intuition to a more rigorous definition. In her book "Artificial Intelligence: A Guide for Thinking Humans", M. Mitchell dedicates a whole chapter to explore what is meant by the term "understanding" via introspection of some daily life activities. She agrees with J. Hawkins in that whatever it ultimately is, surely it must involve the ability to predict the behavior and properties of various aspects of the world.

### Understanding by Analogy

When we are presented with a new concept to learn, we often encounter two situations: either we can see the new concept as an obvious analog of something else we already know, or it seems foreign and we need to spend time analyzing its parts and behavior. In the latter case, we start to understand the concept when we find that its constituent parts have analogs that we already know. For example, when we learn algebra in high school, we use our knowledge of basic arithmetic as a foundation, although we still need to learn the idea of abstracting unknown quantities into variables.

Even after we learn the behavior of individual constituent parts, understanding of a concept may involve something else: the ability to reliably predict how individual parts interact with each other to produce an overall behavior. An example of this is when we learn how to drive a standard car having driven only automatic cars previously. We're already familiar with the gas pedal and brakes, but we need to become familiar with the clutch, and then learn how to coordinate the gas pedal and the clutch when starting up the car to prevent it from stalling.

### Congruence in Predictions

As we learn something new, our usual state of confusion can be regarded as the inability of our incipient mental model to produce a prediction (any prediction). In addition to that, for concepts that are open to multiple interpretations, it may be the case that we do have a prediction but our prediction is incongruent with predictions from other models for the same or related concepts (i.e., the realization that our analogy breaks down at some point).

Consider, for example, how our initial understanding of gravity is first achieved by intuitive learning when we are infants. One thing we intuit is that heavier objects will fall to the ground faster than lighter ones. This level of understanding is useful enough for many human activities, but as Galileo discovered in the 14th century, it is incomplete.

One way in which Galileo refined his understanding of gravity was by designing experiments whose results contradicted his initial hypothesis. In this way, he developed a mental model that correctly predicted how objects would fall to the ground under various circumstances. His model, however, didn't quantify how fast objects would fall to the ground. Later on, Newton would discover a model that explained with great precision this and other things related to gravity, providing congruent predictions for various phenomena under different contexts. This illustrates the idea of "progressively deeper understanding".

{% hint style="info" %}
In summary, we may say that: "to understand something" means "to be able to predict its behavior and properties in one or more contexts". This may happen through a combination of analogy-making and learning of predictive models at one or more levels of abstraction, in one or more contexts.

The more accurate our predictions for the object in question, and the wider the set of contexts in which we can make correct predictions, the better we understand it.
{% endhint %}

## Misconceptions on Understanding

### Binary vs Continuum

It's worth reiterating that "understanding" is not a binary concept. When we first become familiar with something, a basic predictive model develops in our minds, but this model may not provide the most accurate predictions (despite our subjective sense of confidence.) This situation is pretty common, even if we're not always completely aware of it. As we learn more about a concept, both in depth and breadth, that model becomes more precise, allowing for better prediction.

Viewed from this angle, it is possible to argue that all entities capable of processing information have some level of understanding of various things in the world, and this includes not just organisms with brains, but even complex systems that build predictive models of the world as emergent properties (e.g., ant colonies, the immune system).

Animals like dogs and cats may not have such a complex model of the world as humans, but they certainly have a much better model of the world than the most powerful AI/ML models we've built so far. And in some areas (e.g., olfactory modeling of the world), they definitely have much better models than us humans

### Language Is Not Required

Another common misconception about understanding is that, unless we can explain a concept using language, we don't really understand it. This fallacy follows from the misconception that understanding is binary, or that language is the same as thinking. As cognitive scientist S. Pinker [has explained](https://youtu.be/Q-B_ONJIEcE), this is just not true. While language is a fascinating cognitive tool that deserves its own analysis, it is known that it is not an absolute prerequisite to intelligence (and therefore to understanding).

{% hint style="warning" %}
This is not to say, however, that language plays no part in the development of deeper understanding in humans and animals. It is quite likely that language does have a strong influence by helping us augment our working memory, hone the precision of our thoughts, and increase the exchange of ideas with others.
{% endhint %}

A quote often cited is that "If you can't explain something in simple terms, you don't really understand it". A better formulation of this would be "The better you understand something, the more you can explain it in simple terms."
