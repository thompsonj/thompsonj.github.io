---
layout: "post"
title: "Towards a common philosophy of explanation in AI and neuroscience. Part II"
date: "2018-04-05 17:17"
comments: true
categories: []
---
# Part II: Dominant theories of scientific explanation

As a researcher, the choices you make about what questions to ask, what experiments to perform, what measurements to make, what tools to use and how you interpret your results imply answers to philosophical questions about the nature of the phenomena you study and how it should be understood. Whether you choose to interrogate these assumptions or not, they are there. My general impression is that most graduate training in science does not train us to do this kind of interrogation. We are trained to *do* more than to *think*. If you join a research group as a first year masters or PhD student, you will likely learn to conduct experiments similar to those that were previously conducted in the same group. It's easy to become entrenched in a particular approach and yet not be able to rigorously justify it because you've never been asked to do so.

What is your answer to the question "Why are you doing that experiment?" Part of what philosophers of science do is take how scientists motivate and describe their work and turn it into rigorous theories about how science works, how it progresses, what distinguishes science from non-science, and how to best explain different types of phenomena. My goal with this post is to provide some background in the philosophy of scientific explanation of neural and computational systems to better equip us to express our views on questions like 'how ought intelligence be explained?', and ultimately to be able to design experiments that we can rigorously justify.

## Background
To begin, we assume that the goal of science is to know and understand our world. A primary goal of science is to provide explanations of phenomena (be they natural, social, or otherwise). The role of a theory of scientific explanation is to characterize the structure of explanations in science. An account of scientific explanation must distinguish between explanations that are scientific and those that are not. It must also distinguish between explanations and non-explanations. Sometimes this second contrast is presented as the difference between explanation and description. For example, a set of claims about the appearance of a particular species may be true, accurate and supported by evidence without being explanatory in any way. They are "merely" descriptive. (paraphased largely from [[1]](https://plato.stanford.edu/entries/scientific-explanation))

I think an important but neglected piece of scientific litteracy is the ability to look at a set of claims or a model and decide whether it is descriptive or explanatory (or neither) according to your favorite theory of scientific explanation. At the same time, I don't want to suggest that description is somehow inherently less valuable than explanation. We must know that a phenomenon exists before we can ever hope to explain it. In calling for better litteracy of theories of explanation, my wish is not to reduce the amount of descriptive science, but rather to reduce the mispresentation of scientific activities. When you claim that your work is explanatory, when actually it is descriptive according to any contemporary theory of scientific explanation, you slow down science. If we already think that we are explaining, then we will not spend time figuring out how to expalin. Instead, if we acknowledge that what we are currently doing is descriptive, we can better see our role in a larger scientific enterprise, i.e. the role of a particular series of experiments may be to describe a specific set of phenomena that may later be explained by different types of experiments. When our perceived explanatory power is inflated, we're closed off from seeing how we might work together to ultimately better explain.


## Theories of Scientific Explanation
## The Deductive-Nomological (DM) Model
_aka Hempel's model, the Hempel–Oppenheim model, the Popper–Hempel model, or the covering law (CL) model_
Scientific explanation consists of the _explanadum_, which describes the phenomena to be explained, and an _explanans_, which accounts for the phenomena (Hempel 1965 cited in Woodward 2017). According to this theory, the explanans successfully explains the explanadum if several conditions are met:
1. “the explanandum must be a logical consequence of the explanans” (Hempel 1965 cited in Woodward 2017). An explanation is the deductive argument that shows that the explanadum is expected given the premises of the explanans.
2. The explanans must rely on at least one "law of nature" in its explanatory logic.

Hempel uses the term "law" to differentiate deterministic laws from other true generalizations that are only "accidentally true" (see Woodward 2017 for examples). Unfortunately, no agreement about how to define this notion of lawhood has emerged in the decased since the DN model was proposed. Additionaly, many generalizations that are central to explanation in the special sciences (biology, psychology, economics, etc) fail to satisfy any of the standard criteria for lawfulness. Are laws only present in physics? How then would the DN model apply to explanations in the special sciences?

Hempel also recognizes deductive-statistical (DS) explanation which rely on statistical laws instead of deterministic ones, and inductive-statistical (IS) explanation: "an IS explanation will be good or successful to the extent that its explanans confers high probability on its explanandum outcome" (Woodward 2017). According to all DN variants, “the essence of scientific explanation can be described as nomic expectability—that is expectability on the basis of lawful connections” (Salmon 1989, p. 57).

There are a number of well known counter examples to the claims that the DN model provides necessary or sufficient conditions for explanation.
* Explanatory asymmetries: derivation of an explanadum from a law and initial conditions can meet the critier for a DN explantaion, while the reverse derivation of initial conditions from the explanadum and law is not explanatory. The DN model doesn't account for the fact that some explanations are directional.
* Explanatory Irrelevancies: A derivation may satisfy the DN model, while relying on a true generalization that is irrelevant to the explanadum.


## The Statistical Relevance (SR) Model
The Statistical Relevance (SR) model (Salmon 1971) is an attempt to capture the features of causal or explanatory relevance that elude the DN model variants. Statistical relevance here refers to conditional dependence. The main claim is that explanatory properties are statistically relevant. "Given some class or population \\(A\\), an attribute \\(C\\) will be statistically relevant to another attribute \\(B\\) if and only if \\(P(B∣A.C)≠P(B∣A)\\)—that is, if and only if the probability of \\(B\\) conditional on \\(A\\) and \\(C\\)is different from the probability of \\(B\\) conditional on \\(A\\) alone" (Woodward 2017). This tackles head on the problem of explanatory irrelevancies in the DN model. Notice though, that an explanation is no longer an argument, as in the DN model. Here, an explanation is a collection of information that is statistically relevant to the explanadum. A consequence of this model is that an explanation need not make an expanadum expected. A high probability event (e.g. a biased coin toss landing on heads) and its alternative low probability outcome (landing on tails) are both explained by the same explanans (the bias of the coin and the action of tossing).

relies on condition of objective homogeneity, that "there are no additional omitted variables that would affect the probability" which is rarely met in most interesting problems. Maybe true for studying quantum mechanics in controlled experiments, but not for things like trying to explain recovery from illness or juvenile delinquency.

in QM, assumption that the phenomena of irreducibly indeterministic
## The Causal Mechanical (CM) Model
“mechanisms are entities and activities organized such that they exhibit the explanandum” (Craver 2007)
explanation is "a matter of showing how a phenomenon is produced by its causes", of situating a phenomenon in the causal structure of the world
two types:
etiological: explanation in terms of antecedent causes, e.g. virus causes flu, dehydration causes thirst
constitutive (or componential): describe underlying mechanisms
### Norms of constitutive mechanistic explanation
Reductive tradition
understanding is the rational expectation of a phenomenon at one level from laws governing parts at a lower level
Systems tradition
explanation is the matter of decomposing a system into its parts and demonstrating how those parts are organized in such a manner that they exhibit the phenomenon to be explained.
“If you can’t make one, you don’t know how it works”
“you need a blueprint, a recipe, an instruction manual, a program” (Dretske 1994: 468)
Organization is important:
not just the sum of parts but their interaction
separate how-possibly from how-actually
### Aspects of mechanistic explanation (Craver 2007)
the nature of the phenomenon to be explained
the constitutive relationship between a phenomenon and its components
the difference between real components and useful fictions
the nature of capacities or activities
the nature of mechanistic organization
the nature of constitutive explanatory relevance

## Functional Explanation (Cummins 1975, 1983)


## Representational
Paul Churchland


## Unification Model

## Mechanistic Explanation

## Network Science
Useful for explaining non-decomposable systems, where part-whole decompostion is not possible.
Does not use idealization to simplify, rathere "explits the very properties that make a system complex [...] to furnish new forms of explanation." (Rathkopf 2018)

Levy and Bechtel say network analysis is a continuation of mechanistic analysis. Rathkopf argues instead that network science represents a departure from the mechanistic approach.





<!-- ### H3
#### H4
##### H5 -->

## References

Woodward, James, "Scientific Explanation", The Stanford Encyclopedia of Philosophy (Fall 2017 Edition), Edward N. Zalta (ed.), <https://plato.stanford.edu/archives/fall2017/entries/scientific-explanation/>

Brian Cantwell Smith The philosophy of computation meaning, mechanism, mystery <https://www.youtube.com/watch?v=USF1H70bRl0&lc=z12jujiqnqjpylwcr23ft5jpetaugfrne.1524097262271529>

Ilya Nemenman, Playing Newton: Automatic Construction of Phenomenological, Data-Driven Theories and Models at Workshop on Computational Theories of the Brain <https://simons.berkeley.edu/workshops/schedule/5386>
