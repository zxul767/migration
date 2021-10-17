---
description: Does our mind run a partial simulation of the world?
---

# Models of the World

## TODO

* [ ] Review section Feature Discovery and complete it

## A Partial Simulation of the World

The idea that our mind is like a society of predictive models for many aspects of the world is very compelling, since it offers a plausible explanation for many cognitive capabilities we observe in intelligent organisms. It has been thought up by several AI researchers before, including M. Minsky (in "The Society of Mind") and J. Hawkins (in the "Thousand Brains Theory").

Not everyone agrees exactly on how these models are organized, though. In the Society of Mind,  M. Minsky argues for a diversity of mental processes organized in various cognitive layers similar to a society. In his own words:_"What magical trick makes us intelligent? The trick is that there is no trick. The power of intelligence stems from our vast diversity, not from any single, perfect principle."_  

On the other hand, based on strong evidence from neuroscience, J. Hawkins believes that there is one master algorithm replicated throughout the neocortex, which is sufficiently flexible to encode the most important mental processes that give rise to intelligence.

In both of these theories, the basic premise seems to be that our mind is running some sort of partial simulation of the real world triggered by either external stimuli or memories (i.e., internal stimuli). This aligns well with the ideas we've outlined in [On Understanding](../intelligence-1/understanding.md), and also explains well several other mental processes, such robust object recognition, reasoning, general problem solving, imagination, and perhaps even creativity to some extent.

In this view, thoughts are the processes that run the partial simulation of an internal world that tries to mirror the external world we live in. Consequently, our thoughts are not only those processes we're able to introspect (i.e., the ones we usually think about when we think of thoughts), but also the ones that don't bubble up to our consciousness, but which are nonetheless crucial, and perhaps in many cases even more important than the ones we can introspect.

{% hint style="info" %}
It is almost a cliché about inventors, scientists and artists throughout history, that many of their breakthrough ideas came to them while they were not consciously thinking about them (e.g., in sleep-like states or distracted doing something else). 

Kekulé, the German chemist who discovered the structure of the benzene molecule, spoke of the creation of the theory, saying that: "_he had discovered the ring shape of the benzene molecule after having a reverie or day-dream of a snake seizing its own tail (an ancient symbol known as the ouroboros)." _
{% endhint %}

## Ensembles of Models is a Recurrent Idea

The intuition behind all these theories is that it's very useful to get multiple views of a concept to better understand it. It is a pervasive idea that shows up again and again in various forms. In everyday life, we use it when we discuss issues with a diverse set of people; in ML, we use it in ensemble models such as Random Forests and Boosting Trees. The details vary, but the basic idea is always the same.

When we consider how evolution has created organisms of such incredible complexity, one compelling hypothesis is that in many cases an organism was the result of the symbiosis of two smaller organisms. In some cases, this symbiosis turned out to be so intricate and successful that it eventually became a single organism. Of course, this amalgamation most likely required some coordination to work well, and perhaps that's one way in which primitive brains originally evolved.

If we accept the premise that our minds are indeed building and using models of the world, the next natural question is how are such models represented and learned raw sensory input. Two very intuitive things to consider are objects and the relationships between them.

## Objects and Relations

We have so far used the words “objects” and “relations” by appealing to their intuitive meanings, but as we start to dig deeper into the idea of models of the world as a foundation for most of our cognitive abilities, we need to start being more precise.

Intuitively, we tend to view the terms “object” and “relation” as related but clearly distinct. Objects seem to be things that stand on their own, common patterns that show consistency in space and time, things that have a recognizable identity and a name attached to them. Relations, on the other hand, seem to always require two or more objects, and don’t necessarily have a name attached to them. However, if we observe various examples of them carefully, it's not hard to accept that relations can also be understood as objects, and objects as relations.

### The Objects-Relations Duality

It's easy to see that most objects are either composed of other objects or their definition necessarily relies upon other objects. Viewed this way, a big part of what defines an object is not just the individual parts that compose it, but also the way in which they are organized, i.e., the way they relate to each other.

{% hint style="info" %}
Intuitively, anything that has identity (i.e., it can be told apart from other objects or class of objects) by virtue of showing consistent patterns across time, can be considered an object. 

At the highest level, dogs and rain have in common the fact that they both display consistent patterns across time (e.g., a dog's physical shape remains pretty much constant over time and so do its basic behaviors; rain is water falling from the sky in more or less the same way). It is this abstract consistency that enables our minds to distinguish and classify them as individual objects.
{% endhint %}

It is not too far-fetched to think of relations as a defining characteristic of objects. In other words, objects can be viewed as graphs of their constituent parts, where the nodes represent the "smaller" objects, and the edges the relations (e.g., temporal, spatial) between them. 

{% hint style="info" %}
D. Hofstadter has expressed a closely related view, albeit stretched to the idea of analogies, that is summarized as_"without concepts there can be no thought, and without analogies there can be no concepts"._

In D. Hofstadter's view, analogies are the parallels we draw between the "skeletal essences" of objects, thanks partly to our ability to "see" not just their direct identity, but also the things they have in common with other objects, sometimes small and direct, sometimes subtle and abstract. One plausible explanation of how our brain does this is by finding isomorphisms between graphs that constitute such skeletal essences in various objects.
{% endhint %}

To give an example of this idea, consider how a vehicle can be seen, in an abstract way, as the combination of wheels, a steering device, and some other object to “seat” passengers. However, notice that the relations between some of these elements matter. Wheels are expected to be at the bottom making direct contact with the ground, in a vertical position; the “seating” object attached on top of the wheels; and the steering device on top, attached to this ensemble, in such a way that it’s easy to manipulate for a passenger.

Of course, spatial relations are not the only thing to consider in a general framework for object recognition (though it may be enough for many tasks.) Temporal relations combined with spatial relations can significantly enrich the power of object recognition models. Think, for example, how it is often possible to recognize a person from far away (even when all we have is a low resolution image that would be insufficient on its own) by observing how they walk. The specific way they move (a combination of spatial and temporal patterns) is often mappable to the identity of the person.

Likewise, other kinds of relations can be extremely useful to identify intangible objects. Imagine walking into a room where there’s some social tension. How does your brain recognize such a situation? Surely the individual postures and expressions of the people involved may provide hints, but it’s mostly the presence of other higher-level patterns in the room--best described as interactions, or relations, between people--that betrays what’s going on. For example, the passive aggression between two individuals, or the intimidating stare from one person to another.  

Some people might label this as "situation recognition", but "object recognition" or "concept recognition" seems like an adequate term if we acknowledge that objects, beyond our intuitive notion of them, can also refer to relations and situations (i.e., collections of relations).

Conversely, when certain relations become common enough, it is reasonable to consider them as objects. After all, their consistency over time gives them an identity, and a name for them is usually developed. “Love” (perhaps understood as a collection of relations among various objects, such as “care”, “respect”, etc.) is one example; "Passive Aggression" is another.

### Objects as Relations in AI Models

Despite the conceptual simplicity of these ideas, few AI systems have directly incorporated these ideas throughout the history of the field. It should be noted, however, that most current systems do acknowledge them partially or in implicit ways.

Some early attempts include programs derived from the "Active Symbols Cognitive Architecture" (first proposed by D. Hofstadter), of which the Copycat program (developed by M. Mitchell) is perhaps the most famous one. 

Copycat, although intended for the problem of analogy-making and restricted to a much simpler artificial domain, makes use of a network of concepts (i.e., relations between objects) to try and discover analogies automatically. In some ways, its functioning is similar to CNNs in that it tries to identify local features in order to recognize larger concepts which can help to build analogies. Unlike CNNs, however, Copycat's search for features is aided by its (pre-defined) network of concepts, and requires almost no training (at the expense of many built-in priors).

In modern ML, CNNs build collections of features in a hierarchical way, but they don't establish a graph a relations between them. Similarly, Naive Bayes classifiers build so-called "bags of words" as features for text classification, but they ignore the relationships between words.

More recent developments, however, are resurfacing this important idea. Attention models--first developed in the context of NLP--use the relations between constituent parts as a way to improve predictions. Others, like Capsule Networks, directly model spatial relations between constituent parts to improve classification robustness in the face of rotations and other distortions in the input.

In reflecting about the limitations of many current ML models (see [What CNNs Get Wrong](../abstraction-1/what-cnns-get-wrong.md)), we realize that learning relations among abstract features or objects is crucial to build more robust systems that can perform the feats of abstraction and analogy that we routinely observe in humans. However, the best way to do this efficiently and effectively from raw sensory input remains an open problem.

## Features and Patterns

The word “feature” has been used quite a lot in these pages, but we haven’t really described it in detail as we’ve assumed it’s intuitive enough. However, in conjunction with other words such as “objects” and “patterns”, its distinction or relation to those other concepts may no longer be so clear.

{% hint style="info" %}
In a very general context, a feature is any aspect of an object that can form the basis for a good representation of the object that allows us to solve one or more tasks more easily.
{% endhint %}

In the context of object recognition, a feature is any salient aspect about the object that has some predictive power in its identification. In a compositional world as ours, this may include constituent objects (e.g., a bicycle may have as features wheels, a steering bar, a seat, etc.), but also other patterns which don’t have a name because perhaps they’re not common enough to deserve one (e.g., the peculiar shape or texture of a rock). 

It is perhaps obvious that the constituent parts of an object are salient aspects about it, but this does not necessarily mean that every such constituent object is more important than other nameless features. For example, the distinction of dalmatian dogs from other breeds of dogs is perhaps best achieved by looking at their fur patterns. Although we have no universal name for such a pattern (we usually just call it “spots” if pressed to describe it), it’s not difficult to see why it’s a powerful predictive feature in this case.

The word “pattern”, often used in connection with the word “feature”, is both more basic and more general. A pattern is a term used to describe an arrangement of things that is consistent over space and time. In this sense, it has an overlapping definition with “object”, but the latter is often used when the pattern is large and common enough for us humans to directly perceive it as an independent unit in this world.

If you feel there's some circularity in these definitions, you're absolutely correct. After all, if an object is just a very high-level pattern, and objects are made of other smaller objects, which in turn can be described through features (which are patterns themselves), it's clear that it's patterns all the way down. Not surprisingly, some people think that pattern recognition is the fundamental pillar to solving cognition.

### Feature Discovery

One intriguing question is how are object features discovered: are they intrinsic in objects? or are they always relative to a context (i.e., to the tasks for which they are useful)?

When the features of an object are first-class objects themselves (e.g., a nose in a face), it's intuitive to think that they must be intrinsic to the object (i.e., they define it), and that an object always has a unique set of features. But consider, for example, that while for us humans the redness of an apple is a very useful feature to identify it, for a dog (which is dichromatic and can't distinguish redness) it is actually its smell that's the most useful feature.

What this means is that, in reality, an object may have one or more "projections" (e.g., certain light wavelengths bouncing off of it) which, depending on our ability to capture them, will end up as "visible features" for us. Even when our senses are able to capture all of them, it is almost always the case that evolution induced in us a bias to perceive as more salient those features which are useful to survive in certain environments (e.g., our ability to perceive certain light wavelengths and interpret them as "bright colors" was probably useful to avoid certain poisonous flowers or animals).

On the flipside, it is also possible that our ability to perceive certain object features wasn't always due to evolutionary pressure. It is conceivable that genetic mutations and sexual recombination of genes could have lead to abilities which were not immediately advantageous, but which proved very useful in the future under different circumstances. It has been argued, for instance, that consciousness wasn't necessary for our species to survive, but it could have evolved as a byproduct of one or more mutations that affected our brain's architecture.

Analogously, perhaps the discovery of relevant features in ML models must not always be tied to specific tasks (as we have done for the most part in supervised learning.) There is some evidence to this effect in reinforcement learning experiments where agents develop skills that appear to generalize well across different tasks. To achieve this, they are simply allowed to learn features of the environment guided by some induced notion of "curiosity" instead of the usual pressure to excel at one specific task.

* Features with more stability (less variance across the population) are likely to be candidates among those that will turn out to be more useful for abstract representations
