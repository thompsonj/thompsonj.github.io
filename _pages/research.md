---
layout: page
title: research
permalink: /research/
description: Themes in my past, current, and future work.
nav: true
nav_order: 0
---

My research spans cognitive science, computational neuroscience, deep learning, AI alignment, and philosophy of science. Below are the main themes, with related papers and open questions.

<style>
.theme-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 1rem; margin: 1.5rem 0 2.5rem; }
.theme-card { display: block; overflow: hidden; padding: 1.1rem 1.2rem; border: 1px solid var(--global-divider-color); border-radius: 0.5rem; color: inherit; text-decoration: none; transition: border-color 0.15s, transform 0.15s; }
.theme-card:hover { border-color: var(--global-theme-color); transform: translateY(-2px); text-decoration: none; color: inherit; }
.theme-card img { display: block; width: calc(100% + 2.4rem); max-width: none; height: auto; aspect-ratio: 16 / 9; object-fit: cover; object-position: 60% 45%; margin: -1.1rem -1.2rem 1rem; }
.theme-card h3 { font-size: 1.05rem; margin: 0 0 0.5rem; color: var(--global-theme-color); }
.theme-card p { font-size: 0.9rem; margin: 0; }
</style>

<div class="theme-grid">
  <a class="theme-card" href="#computational-modelling-of-learning-and-generalization">
    <img src="{{ '/assets/img/dualstream_model.png' | relative_url }}" srcset="{{ '/assets/img/dualstream_model-480.webp' | relative_url }} 480w, {{ '/assets/img/dualstream_model-800.webp' | relative_url }} 800w" sizes="(max-width: 600px) 100vw, 320px" alt="Diagram of the dual-stream neural network model, combining glimpse contents ('what') and glimpse positions ('where')" loading="lazy" style="object-fit: contain; background: #fff;">
    <h3>Computational modelling of learning and generalization</h3>
    <p>How do people and neural networks learn and transfer knowledge to new situations?</p>
  </a>
  <a class="theme-card" href="#behavioural-cloning-to-improve-human-learning">
    <img src="{{ '/assets/img/behavioural_cloning.jpg' | relative_url }}" srcset="{{ '/assets/img/behavioural_cloning-480.webp' | relative_url }} 480w, {{ '/assets/img/behavioural_cloning-800.webp' | relative_url }} 800w" sizes="(max-width: 600px) 100vw, 320px" alt="Diagram of behavioural cloning: a clone trained on human behaviour interacts with an artificial agent" loading="lazy" style="object-position: center;">
    <h3>Behavioural cloning to improve human learning</h3>
    <p>Using machine-learned models of people to discover better ways to learn.</p>
  </a>
  <a class="theme-card" href="#philosophy-of-science-and-metascience">
    <img src="{{ '/assets/img/ai-science-network.png' | relative_url }}" srcset="{{ '/assets/img/ai-science-network-480.webp' | relative_url }} 480w, {{ '/assets/img/ai-science-network-800.webp' | relative_url }} 800w" sizes="(max-width: 600px) 100vw, 320px" alt="Illustration of a network of people connected to an AI system" loading="lazy" style="object-fit: contain; background: #fff;">
    <h3>Philosophy of science and metascience</h3>
    <p>How does science work, and how is AI changing it?</p>
  </a>
  <a class="theme-card" href="#a-cognitive-science-approach-to-value-alignment">
    <img src="{{ '/assets/img/communion_vs_agency.png' | relative_url }}" srcset="{{ '/assets/img/communion_vs_agency-480.webp' | relative_url }} 480w, {{ '/assets/img/communion_vs_agency-800.webp' | relative_url }} 800w" sizes="(max-width: 600px) 100vw, 320px" alt="Violin plots comparing agency and communion scores for reward models built on Gemma and Llama" loading="lazy" style="object-fit: contain; object-position: 34% 50%; background: #fff;">
    <h3>A cognitive science approach to value alignment</h3>
    <p>What values are encoded in the reward models used to align language models?</p>
  </a>
  <a class="theme-card" href="#intrinsic-motivation-and-metacognition">
    <img src="{{ '/assets/img/practicing_piano.jpg' | relative_url }}" srcset="{{ '/assets/img/practicing_piano-480.webp' | relative_url }} 480w, {{ '/assets/img/practicing_piano.jpg' | relative_url }} 728w" sizes="(max-width: 600px) 100vw, 320px" alt="A hand playing piano keys" loading="lazy" style="object-position: 50% 65%;">
    <h3>Intrinsic motivation and metacognition</h3>
    <p>How aware are learners of their own progress, and how does that influence what they decide to do?</p>
  </a>
  <a class="theme-card" href="#collective-learning-in-epistemic-communities">
    <img src="{{ '/assets/img/collective_intelligence.png' | relative_url }}" srcset="{{ '/assets/img/collective_intelligence-480.webp' | relative_url }} 480w, {{ '/assets/img/collective_intelligence-800.webp' | relative_url }} 800w" sizes="(max-width: 600px) 100vw, 320px" alt="One person versus many, with the text 'Human intelligence is collective intelligence'" loading="lazy">
    <h3>Collective learning in epistemic communities</h3>
    <p>When do groups become wiser than their members, and when do they go astray?</p>
  </a>
</div>


## Computational modelling of learning and generalization

People can learn something in one setting and apply it flexibly in another. I build neural network models to understand the computational principles that make this kind of generalization possible in humans and machines, and why it sometimes fails.

Deep neural networks modelled on the brain's ventral visual stream have provided a powerful framework for understanding object recognition, but they struggle with relational aspects of a scene, such as counting the number of items in an array. Inspired by the dorsal stream, we built a "dual-stream" neural network that combines what it is looking at with where it is looking. The network can count wholly novel items ("zero-shot" counting), develops number codes that resemble those recorded in macaque posterior parietal cortex, and makes successful predictions about human gaze during counting. [Zilu Liang](https://www.psy.ox.ac.uk/people/zilu-liang) is currently leading follow-up work extending this model to more challenging visual relational reasoning tasks.

Learning new things can also interfere with what we already know. In work led by [Eleanor Holton](https://eleanorholton.github.io/), we found surprisingly similar patterns of transfer and interference in humans and neural networks learning tasks in sequence. In both, prior knowledge speeds up learning of a similar new task, but at the cost of greater interference with the old one. People also differ: "lumpers" show more interference alongside better transfer, while "splitters" avoid interference at the cost of worse transfer. Neural networks trained in "rich" or "lazy" learning regimes reproduce these two profiles.

<div class="publications">
{% bibliography --group_by none --query @*[key=thompson2024zero || key=thompson2022learning || key=holton2026humans || key=summerfield2023thinking] %}
</div>

## Behavioural cloning to improve human learning

Behavioural clones are machine learning models trained to reproduce human behaviour. Because they can be run quickly, cheaply, and at scale, they make it possible to simulate how people would respond to many possible interventions, and to search for ones that work before testing them with real people. [Past work](https://www.nature.com/articles/s41467-025-58043-7) has shown that this approach can discover novel solutions to social problems. I am currently involved in a number of projects applying it to learning problems, including one focused on accelerating human language learning, which I presented at the [Behavioral Clones Workshop](https://machinebehavior.science/behavioral-clones-ws) in Berlin in 2026. In my own lab, I plan to apply this methodology to social learning problems.

## Philosophy of science and metascience

As scientists, we can't avoid philosophy of science. It shows up whenever we choose a research question (why is this a good question to ask?) or justify a contribution (why does this count as progress?), and in how we design our scientific institutions (peer review, hiring and promotion, how funding is allocated). Sometimes new methods or discoveries transform how science works, and philosophy of science can help us understand those transformations and make good choices in light of them. I am especially interested in how AI is transforming the psychological and brain sciences and, with the rise of large language models, science more broadly. I have written about the nature of scientific explanation in NeuroAI and, with [William D'Alessandro](https://sites.google.com/view/william-dalessandro/home), about the promise and perils of AI surrogacy in psychological research.

My thinking has been shaped by feminist philosophers of science, who emphasize the social nature of scientific knowledge. I find these perspectives compelling and underappreciated. I have written about them in reviews for _Science for the People Magazine_ of Helen Longino's [_Science as Social Knowledge_]({{ '/blog/2024/the-deep-sociality-of-science/' | relative_url }}) and of Robin Wall Kimmerer's [_Braiding Sweetgrass_]({{ '/blog/2024/covenant-of-reciprocity/' | relative_url }}), which brings Indigenous and scientific ways of knowing together.

When we understand how science works, and where and why it fails, we can make it work better, both through our choices as individual scientists and in how we run our scientific institutions. Science policy often reinforces harmful myths that stem from misunderstandings of how science works, such as the myth of value neutrality or the myth of the lone genius. I am interested in philosophy of science and metascience that sheds light on how best to organize and direct scientific communities, especially as machine learning and AI transform them. Scientific communities are one example of the [epistemic communities](#collective-learning-in-epistemic-communities) I hope to study in my new group.

<div class="publications">
{% bibliography --group_by none --query @*[key=d2025ai || key=thompson2021forms || key=thompson2018towards] %}
</div>

## A cognitive science approach to value alignment

Large language models are aligned with human preferences using reward models: networks trained on human ratings to score how good a response is. Reward models therefore decide which values end up in the final system, yet they are rarely studied directly. In collaboration with [Brian Christian](https://brianchristian.org/) and [Tsvetomira Dumbalska](https://tsvetomira-dumbalska.github.io/), we develop methods informed by cognitive science and psycholinguistics to study reward models. We probe a reward model's values by searching its entire vocabulary for the "optimal" and "pessimal" tokens in response to value-laden prompts. Applying this method to open-source reward models, we found that they inherit value biases from the pretrained models they are built on. For example, words related to Agency are ranked higher by reward models built on Llama than by those built on Gemma, while words related to Communion are ranked higher by those built on Gemma, even when the models are fine-tuned on identical preference data. We also found that tokens associated with race, ethnicity, and sexuality were often assigned very low scores, regardless of how the prompt was framed. This is consistent with previously documented cases of linguistic erasure, in which language models avoid certain terms because they were overrepresented in negative examples during alignment training.

There are several possible future directions:

- **Personas.** How stable are the values reflected in reward models or do they adapt to the user?
- **Downstream consequences.** Do these biases causally shape the behaviour of the final, preference-tuned language model? For example, would a model asked about the most common cancers downweight "breast" because of the word's association with pornography?
<!-- - **Beyond US models.** Both Llama and Gemma were developed in the US. How do reward models built on European, Chinese, or other foundation models compare in the values they encode? -->
- **Measuring preferences well.** Our results suggest that the design and documentation of preference datasets deserve much more attention. What exactly were human raters asked, how, by whom, and in what context? Even publicly available preference data usually lacks this information. Psychologists are experts in designing human experiments to reveal latent mental states, and AI research could benefit from that expertise.
- **Transparency.** We could only study open-source reward models because the reward models behind proprietary systems are not available. Yet users may reasonably want to know what values a system was optimized for before choosing to use it, and at present they have no way to find out. One option is to require developers to publish a profile of the reward model used to optimize any system they release, a kind of nutrition label for an AI's values.
- **Context-sensitive wellbeing evaluations.** People increasingly turn to AI to talk through existential worries, such as anxiety about climate change. Climate anxiety is often a rational response rather than a pathology, so a good response validates concern without escalating it and supports constructive coping. I am interested in building evaluations, grounded in psychological research on coping, that measure whether AI systems handle this well.
- **Who contributes, and who benefits.** AI is built from human behaviour, in the form of data, preferences, and feedback, yet that contribution is largely invisible. I'm interested in how cooperative models of AI ownership and governance could make it visible and give the people who provide it a stake in the tools it builds.

<div class="publications">
{% bibliography --group_by none --query @*[key=christian2026reward || key=christian2025reward] %}
</div>

## Intrinsic motivation and metacognition

What makes a task so engaging that we happily spend our free time on it? Why do we voluntarily take on activities that frustrate us? And why do we avoid effort in some situations, yet actively seek it out in others?

I am collaborating with [Franziska Brändle](https://franziskabraendle.github.io/) and her new group at the University of Giessen to study intrinsic motivation, learning progress, and metacognition, using computational modelling and large-scale naturalistic datasets. We will begin by asking how accurately learners can track their own learning progress, and how well they can predict the effort and enjoyment a task will bring. We then want to understand how these judgements combine to guide what activities people choose to engage in. We are also interested in comparing curricula designed to maximize learning progress with curricula designed to maximize engagement, to tease apart what keeps someone on task from what helps them learn fastest.

## Collective learning in epistemic communities

Much of what any of us knows, we learned from other people. Communities of scientists, students, colleagues, activists, and citizens form beliefs together: they share evidence, trust and defer to one another, and argue. Sometimes they converge on the truth, and sometimes on error. I want to understand the computational principles that make some epistemic communities wiser than their individual members, and others less wise. Questions I hope to pursue include:

- **The wisdom of crowds and the madness of mobs.** When does learning from others improve a group's judgements, and when does it amplify errors and biases?
- **Learning by teaching.** Often, the best way to learn something is to teach it. Why does teaching help the teacher learn? And do effective pedagogical approaches work, in part, by training groups of learners to teach themselves?
- **Who should talk to whom, and when?** How does the structure of a community (who talks to whom, who is trusted, how diverse its members are) shape what it comes to believe? I plan to use [behavioural cloning](#behavioural-cloning-to-improve-human-learning) to discover communication schedules and network structures that serve a community's goals, such as speed, robustness, or objectivity.
- **Organizing for collective problems.** Different collective problems may call for different structures. A trade union has a well-defined membership and a clear counterpart to bargain with. A climate movement has diffuse membership, many possible targets, and a goal, cutting emissions, that no single actor can deliver. I would like to connect computational theories of collective learning and coordination to real-world organizing: which structures suit which kinds of problems, and do groups organized accordingly achieve more change?
- **Collective agency.** Many people have learned from experience that their individual actions make little difference. Acting with others may undo this learned helplessness by revealing the power people have together. Can taking part in collective action foster a sense of collective agency and hope?
<!-- I want to test whether taking part in collective action builds a sense of collective agency and identity, and whether it fosters hope, because participants begin to see how change can happen and how they can contribute. If so, collective action may be an especially effective way of coping with climate anxiety. This is in line with recent research which found that doing something constructive and seeking social support and meaning were effective strategies for students coping with climate anxiety ([Hill-Harding et al., 2026](https://eprints.gla.ac.uk/385665/)). -->
- **Collective intellectual humility.** What kinds of environments encourage a community to recognize and respond well to the limits of its own knowledge?
- **AI governance and democratic institutions.** How does the way AI is owned and governed, whether by a few companies or by the communities that use it, shape what those communities are able to learn and how they coordinate? And could AI itself help us build more democratic institutions?
- **When what helps individuals harms the community.** Something that benefits each individual learner can be bad for the epistemic community as a whole. For example, generative AI may make individual scientists more productive, but if everyone relies on the same AI systems, the hypotheses scientists test and the explanations they offer may become less diverse, at a time when [science is already becoming less disruptive](https://doi.org/10.1038/s41586-022-05543-x). I plan to use agent-based models of epistemic communities to study effects like this, and to identify policies that could prevent them.

This is the newest direction in my research, and the one I most hope to build my lab around. If these questions interest you, please [get in touch]({{ '/join/' | relative_url }}).

<!--
## Earlier work
TODO: deep learning and auditory neuroscience (PhD), music information retrieval.
-->
