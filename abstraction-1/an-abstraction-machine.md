---
description: A proposal to build a classifier that is robust to abstractions
---

# An Abstraction Machine

## TODO

* [ ] Review chapter and add subsections where appropriate
* [ ] Add diagrams where appropriate
* [ ] Explicitly link ideas here to ideas in "Models of the World"

The previous section hinted at two ideas that may constitute the basis for a stronger definition of an “abstraction machine” (a classification model robust to various abstractions of the input), but I’ll elaborate further here and conjecture what I think is needed to build such models.

Any classification model that is robust to various abstracted representations of its input needs to keep an internal representation that:

1. Maintains features extracted at various levels of “reduction” of the original input of an object. For an image, this may mean generating various “distillations”, e.g., discarding color information and textures, performing image erosions, etc. It is not not completely clear how such reductions should be done, but it is likely that they must also be learned for maximum efficacy, as opposed to simply being hard-coded. For example, in the domain of visual recognition, geometric structural features seem quite important, so distillations that focus on that are very important. This is something we intuit due to our close and deep familiarity with the domain. However, if we were to move to a domain of olfactory recognition, we’d probably have a hard time coming up with the right kind of features that are invariant to abstractions. In fact, we may not even have the faintest idea of what “abstraction” looks like in that domain (although we can still rely on the general definition of “detail reduction” to try and imagine it.)
2. Maintains such features in a “probabilistic hierarchy”, reflecting the compositional nature of most real-world objects. This hierarchy should act as an index into the internal representations of an object (which may be anything from a straightforward recording of the input as first perceived by the senses, all the way to a network of symbols that represent the object being classified and its relations in the world.) This idea occurred to me recently, so I consider it provisional. It seems to fit the overall model well, and explains several questions regarding potential storage and retrieval requirements, but I don’t yet have a strong argument for it.

Idea 1 is necessary to be able to classify a single object at various levels of abstraction. For example, any such model should be able to recognize a dalmatian dog as belonging to a very specific class of dogs, but it should also be able to more generally recognize it as simply a dog, and more generally as an animal. Given the right parameters and enough data, such a model would probably figure out other intermediate levels in a hierarchy.

Idea 2 is necessary because it is often the case that objects contain characteristics that belong to one or more general groups at any level of the hierarchy. For example, in a hierarchy that classifies animals according to their ability to fly, walk, and swim (major behavioral features of various animals), a duck would not fit just one of these categories but all three of them with pretty much the same probability.

The human brain is likely to implement such an “abstraction machine” that happens to do both inference and training/learning in a single loop (as opposed to most current DL models, which tend to clearly separate the two phases). As Jeff Hawkins has pointed out in his book “On Intelligence”, our concept of “surprise” is likely to be a manifestation of the model’s internal failure to recognize an object. It is then likely to trigger the necessary learning machinery, perhaps paying more attention to the object in question in an attempt to extract more complex features that help to either recognize the object as a composition of other known objects or features, or to completely start learning a new concept when no existing patterns are found.

## The Features Graph

At each level of the probabilistic hierarchy, a set of features is kept that allows to classify the object in question as belonging or not to a given category. However, as a provisional theory, it seems very likely that such features are stored as graphs, i.e., as relations among features (some of which may be first-class objects, as in the case of eyes, mouth, and ears in a face), or perhaps even as just relations among generic placeholders (as in the example of the happy face given earlier.)

It’s not hard to see the adequacy of the idea of a “features graph” in the domain of visual recognition, where structural relations among geometric objects (the abstractions of constituent objects of a larger object) are important. However, it is not hard to see that this representation is also quite useful in other domains. After all, a graph is simply an organization of pairwise relations among objects which is quite useful in determining an overall “abstraction fingerprint” for the object. Even if the human brain doesn’t really use such a data structure, it seems a very useful tool to use for artificial implementations of the “abstraction machine.” 

If the human visual system is really extracting such high-level concepts as basic geometrics shapes from raw input, one key question is how and why did it evolve to do that? Looking at the filters learned by CNNs, it is clear that they are doing very little in terms of learning such general geometric shapes. This could be blamed on details about the architecture (e.g., relatively large lower convolutional layers could be learning more patterns than strictly necessary for good generalization), but I suspect the real issue could be that learning features for specific tasks can sometimes, counterintuitively, result in lower generalization ability.

Humans, and most other animals capable of recognizing abstractions of objects, may have escaped this curse by evolving in a different environment where both image resolution was significantly lower and only grayscale was available. Under such conditions, simpler but more general vision classifiers (which mostly used features such as geometric shapes) may have been easier to evolve. 

If evolution preserved such models in a hierarchy, along with more complex models based on features only visible in higher resolution and input with more colors, perhaps that could explain why vision systems in modern animals (humans included) seem to have no trouble recognizing simple geometric shapes, and using them to create feature graphs that help to recognize both a cartoon and a picture of a dog as resolving to the same concept. This hypothesis seems plausible seeing as evolution often keeps old artifacts until they prove to be completely useless or a disadvantage to the organism. In this case, the situation would be quite the opposite, as the ability to reason abstractly is likely to play in favor of most organisms. 
