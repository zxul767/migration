# What is Abstraction?

One of the things that is often talked about as a major limitation of DL models is their inability to abstract. 

{% hint style="info" %}
 You can test this for yourself by running a model like Resnet34, using transfer learning to train on a particular category of objects you care about. I tested such a model by fine tuning with pictures of cats and dogs, and ran some experiments. Tests with pictures somewhat similar to those seen during training (i.e., photographs or photo-realistic portraits) seemed to work just fine. However, when I tested against cartoon versions of both dogs and cats (i.e., a task that we know children are able to handle just fine without any prior training, other than having seen real dogs or cats), the model failed completely, showing that it didn’t have a sufficiently robust abstraction mechanism.

Deep inspection of what models like Resnet34 are doing behind the scenes (see this article for details) gives a lot of insight about why this is the case.
{% endhint %}

In a similar vein to our discussion about [Understanding](../intelligence-1/understanding.md), it should be noted that abstraction is a gradient and not a binary concept. In everyday life, for example, some people seem to be better at finding connections between concepts or situations that may appear disconnected at first glance. Whether this is an innate ability or simply the product of enough training is not relevant for the purpose of analyzing the functional parts that an “abstraction machine” must implement.

Abstraction is often understood as the reduction of an object, or our perception of it, to more simplified forms which manage to retain some core identity of the object (often defined as one or more of the categories to which it belongs in a taxonomy, but it may as well be the original object itself, as is the case with a person’s cartoon or any simplified drawing of that person.)

The picture of a person’s shadow is a form of abstraction. We recognize it as mapping to the concept “man”, even though it lacks many features of an actual person. It is also quite generic in that it could potentially map to many concrete people, unless the shadow happened to have retained enough structural information about a particular person we know.

Similarly, when young children draw their family, their representation is usually quite simplified: often just a few stick figures representing the basic geometric structure of a body. And yet our brain has no trouble mapping such simplified drawings to the more sophisticated concept of “person.”

What the shadow and the stick figure both have in common is that they each retain some high-level set of features that map unambiguously to the original object. 

In the case of a shadow, it’s likely to be the contour which reveals the underlying geometry (and sometimes may contain additional information to allow for an even more specific mapping, e.g., that of a known person.) 

In the case of the stick figure, the general geometry of the human body is preserved (i.e., abstractions of a head, a torso, arms and legs, all connected in a specific geometric pattern), allowing for an unambiguous mapping.

\*Talk about a hierarchy of abstractions
