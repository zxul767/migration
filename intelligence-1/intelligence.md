# What is Intelligence?

## TODO

* [ ] Review F. Chollet's Measures of Intelligence ideas
* [ ] Expand section on measures of intelligence

## Key Ideas

{% hint style="info" %}
Intelligence has no generally agreed-upon definition. Historically, its definition has shifted several times as new discoveries have been made.
{% endhint %}

{% hint style="info" %}
A common but overly broad definition is _**"an agent's ability to solve problems."**_ This definition implies that intelligence lies on a continuum, according to how varied is the set of problems the agent can solve.
{% endhint %}

{% hint style="info" %}
A common extensional definition of the above is _**"an agent's ability to learn and apply knowledge to solve problems."**_ Here, learning is the crucial piece as it implies the ability to extend the set of problems the agent can solve over its lifetime.
{% endhint %}

{% hint style="info" %}
There are no generally agreed-upon measures of intelligence. The Turing Test was one of the first proposed measures, but many consider it obsolete. In recent years, some interesting measures have been proposed, based on more recent definitions (see [Chollet](https://arxiv.org/abs/1911.01547))
{% endhint %}

## No Easy Definition

There is no single definition of intelligence that all researchers across various disciplines agree upon. It seems to be a moving target as provisional definitions fall short in the light of new discoveries. For instance, in the 1960s many AI researchers used to think of expert chess play as the epitome of human intelligence, as it was thought to require deep reasoning ability: “surely if we can solve chess, we’ll be well on our way to solving artificial intelligence.” But it only took a few decades for them to realize how wrong this idea was.  

To current researchers, the idea may seem immediately naive but let's keep in mind that "hindsight is always 20/20" and that "any sufficiently advanced technology is indistinguishable from magic". In this regard, cognitive scientist D. Hofstadter has expressed a deep concern for the fact that perhaps what AI research will ultimately prove to us is that we humans aren't really that special. That the cognitive abilities that we thought made us so unique aren't really so hard to imbue in artificial programs after all.

{% hint style="info" %}
On a philosophical note, I find that our ability to have subjective experiences is enough to keep us from adopting a cynical attitude about the world, even if we were to discover without a doubt such things as the nonexistence of free will. What defines our universe might ultimately rest upon a deterministic substrate, but the worlds that arise in the intermediate levels are rich enough to provide us with subjective experiences that are worth living.
{% endhint %}

It's also important to remember that even if an initial idea or development fails to meet our more sophisticated definitions of intelligence, it may still contain the seeds for much more powerful ideas that will form the foundation for intelligent agents that we won't be able to dismiss as "bulldozer intelligence" or "not general intelligence" one day.

{% hint style="info" %}
Some discoveries that appear small or irrelevant at first may turn out to be fundamental building blocks upon more careful revision. The issue is sometimes one of scale. Neural Nets were known for decades before the Deep Learning boom starting in 2012, but the difficulties in scaling them to train on large enough datasets made them seem like an interesting but largely sterile effort. Geoff Hinton, one of the fathers of Deep Learning, tells the story of how he discarded the idea of "dropout" (a regularization technique) soon after he originally conceived it, after seeing that a hasty implementation didn't work as he expected. Later on, he and his students revisited the idea more carefully and finally found a way to make it work.
{% endhint %}

## Provisional Definitions

Perhaps the crudest definition of intelligence we can think of is “the ability to solve problems." However, it’s easy to see that such a definition is too vague and causes issues: a pocket calculator has the ability to solve some arithmetical problems, does that qualify it as intelligent?

Intuitively, what we usually mean by intelligence is not just the ability to solve specific problems, but perhaps more importantly the ability to learn to solve new problems. This is why Deep Blue, despite having been able to defeat the world’s chess champion, wasn’t regarded as truly intelligent by most AI researchers. From this standpoint, learning appears to be a fundamental component of any agent that we may deem intelligent.

{% hint style="warning" %}
On the other hand, as some AI researchers have argued, intelligence should be understood as lying on a continuum. If we accept that, it follows that "bulldozer intelligence" (such as the one displayed by Deep Blue) is also a form of legitimate intelligence: one which can be argued to be doing something very similar to what our imagination does (i.e., simulation of possibilities in a world space).

In this line of thought, it should also be accepted that machines are already more intelligent than most humans on various specific kinds of problems (e.g., numerical calculation, computation of optimal driving routes, recognition of cancer tumors), despite the fact that on a more general plane (and in particular, in our ability to learn new things efficiently), we continue to dominate over them.
{% endhint %}

In the context of living organisms, it is often said that intelligence can be defined as the ability to adapt and survive in a given environment. This definition is, of course, in alignment with the previous one, as the ability to adapt necessarily requires the ability to learn.

Thus, a more general definition for intelligence may be "the ability to learn and apply knowledge to solve problems." While still quite general, it contains two key elements: learning and problem-solving. These two fundamental ideas have spawned a large amount of research, and there remain many problems to be solved, particularly with regards to learning.

## Measures of Intelligence

In his 1950 paper "[Computing Machinery and Intelligence](https://en.wikipedia.org/wiki/Computing_Machinery_and_Intelligence)", Alan Turing proposed that a computer can be said to possess artificial intelligence if it can mimic human responses under specific conditions.

Some current AI researchers still believe this definition is valid, because if the conditions are general enough and the judging criteria well designed, there would be no way for a program with just shallow understanding to pass the test. This implies, among other things, that it would have to be able to perform cognitive functions such as reasoning, analogy-making, and the ability to learn some things rather quickly.

Other researchers think that the Turing's test is too subjective and anthropomorphic, and perhaps not even general enough. More recently, researchers such as F. Chollet have proposed less anthropomorphic measures which are based on an intelligent agent's efficiency to turn raw world sensory input into actionable knowledge which can be used to predict various aspects of the world. This measure is compatible with the last definition of intelligence mentioned earlier, with the implicit assumption that prediction is a fundamental mechanism to solve a large variety of problems. 

By explicitly considering "efficiency" in that "sensory input to internal predictive model" transformation process, Chollet's proposed measure goes beyond Turing's qualitative measure, accepting implicitly the idea of an intelligence continuum, albeit in a more constrained setting (i.e., that of "learning").
