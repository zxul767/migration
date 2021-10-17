---
description: Limitations of the most popular architecture for computer vision
---

# Do CNNs Abstract?

## TODO

* [ ] Review chapter and break into subsections

All current models based on CNNs implement the idea described in the [previous section](abstraction.md) to some extent by learning patterns in a hierarchical fashion (under the reasonable assumption that the world is compositional, and, by extension, so are its visual projections.) However, there are two major issues with these models.

The first issue is that what they learn is based on input that contains too much detail, which conflates both noise and useful signal to uniquely identify an object when presented at various levels of abstraction. Quite often this is mitigated, but not solved to complete satisfaction, by providing such models with a huge amount of training data. This forces the model to reduce the amount of attention it pays to features which don’t show up consistently in most of the training examples.

However, it is very hard to gather enough data that captures all possible projections and abstractions of the underlying object in the real world (i.e., shots from multiple angles, with various degrees of lighting, with occlusion or distortion, drawn as a cartoon, etc.) As a result, the model will be able to recognize objects with certain robustness, but only so far as the test data is close enough to what was seen during its training (in technical terms, as long as the probability distribution during training is the same as that seen when the model is finally deployed.)

The second problem has to do with how these models classify input to a given category based on a weighted vote of features, but without a guarantee that such features are high-level enough, and without taking into consideration that sometimes the relations between such features matter to correctly determine the identity of the object being classified.

These two problems combined show why a model trained on pictures of dogs and cats is unable to correctly classify a cartoon of a dog or a cat. Firstly, during its training the model wasn’t able to capture geometric, structural features of dogs and cats, which prevented it from building abstract representations of heads, legs, and other body parts. Secondly, it didn’t learn that, besides the mere presence of such features, their spatial relations matter; for example, it didn’t learn that a head is usually above the torso, and that arms and legs are connected to the torso in a certain way.

{% hint style="info" %}
One funny way in which you can verify this is by splitting an object’s image into a grid, scrambling the resulting pieces in such a way that is no longer recognizable for a human, and then feeding it to the model. The model will correctly classify it. You may consider this a feature (and indeed, this could be very useful for some applications), but it also reveals the fundamental issue of not learning relationships between features. As we’ll see later, this is more than a mere nuisance in image recognition.
{% endhint %}

![Basic CNNs fail to capture high-level relational information between constituent parts of an object](<../.gitbook/assets/cnn failure mode.png>)

Several researchers have been aware of this problem and have started investigating models that incorporate these ideas. Geoff Hinton, for example, has proposed a model dubbed “Capsules” for visual classifiers, in which information about relative position among objects is recorded. In his “A Thousand Brains” theory of intelligence, Jeff Hawkins has also proposed the need to learn models that use “reference frames” (which capture relations between objects) as a basic building block for prediction models in a mind (he believes that reference frames are not just useful for vision, but also for audio, language and even intangible abstract reasoning.)

The idea of storing relations between objects is fundamental, and seems to be a big part of the definition of objects themselves. It is not hard to see, for example, that many intangible objects are indeed fundamentally relations (e.g., “trade”, a relation between two people exchanging goods), but even with tangible objects one can easily see how the relations among lower-level objects that compose it seem to be the crux of their definition. A face, for example, is ultimately defined by the spatial relations between abstractions of eyes, mouth, and (to a lesser degree) nose. 

This is why we are able to recognize something as simple as a happy face emoticon as representing a face; crude abstractions for the eyes and the mouth are present, but much more importantly, they’re spatially related in the right way. Try distorting that relation by breaking one or more of the spatial relations and all of a sudden our ability to recognize the same object is gone (in this example, changing the meaning completely). 

Interestingly, the abstractions for the mouth and the eyes, when seen on their own, are also equally unrecognizable. This is some evidence for the case that the abstract “definition” of objects (what our brain unconsciously uses to recognize them) is strongly tied to the relations among the constituent parts, and not to the individual identities of the objects.

{% hint style="success" %}
Try this experiment by yourself and notice how moving the eyes and mouth, distorting them into various shapes, etc., doesn't seem to affect your ability to recognize it as a face. You'll be surprised at how general and robust our recognition system appears to be, supporting the idea that it is not faithful detection of eyes or mouth (realistic looking or abstracted drawings) that causes our visual system to recognize a face, but rather the geometric relations between placeholders for those parts.

Of course, this is not the whole story. As I will elaborate in [the next section](an-abstraction-machine.md), it is possible that our visual system uses a hierarchy of features (organized as graphs of relations in each level), to build a more powerful ensemble model. One of the models at the top of that hierarchy is likely to be based on basic geometric shapes and their relations, as this simple experiment suggests.
{% endhint %}
