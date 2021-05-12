# Data Ethics Club: Critical perspectives on Computer Vision
<!--Please don't edit the info panel below-->

:::warning
### :arrow_forward: What's this document?

#### :writing_hand: Let's write together!
We're trying to write up these discussions and include input from everyone.
We hope you'll join us and help us to make any write-ups of the discussion a little more representative of everyone's point of view.

We also hope that through doing this, we'll open up the possibility for more collaborative writing together in the future, e.g. through a perspective article.
That's if there's any appetite from you to do that.

#### :computer: Writing in Markdown
We're using HackMD to write a collaborative Markdown document. 
Markdown is a format for writing text that displays nicely on websites.
On the left you can edit, and on the right you can see view.

#### :grey_question: Getting Markdown help
There is a question mark symbol at the top of the screen that will bring up a cheat sheet, e.g. *write between single asterixes to write in italics* **or double asterixes for bold**.
You can also use the buttons at the top of the edit panel.
:::

## Welcome
Hi :wave:, welcome to Data Ethics Club! 
Thank you for being here!

Link to our [Code of conduct](https://github.com/very-good-science/data-ethics-club/blob/main/code_of_conduct.MD)

## Introductions
Please introduce yourself here.
Feel free to use a pseudoname (this is a public document).
If you provide a GitHub username, I'll use those to credit you for discussions :speech_balloon: and/or writing :writing_hand:  on our GitHub 

__Name, Job title, Affiliation, GitHub, Twitter, Emoji to describe your day__
- Natalie Thurlby, Data Scientist, University of Bristol, [NatalieThurlby](https://github.com/NatalieThurlby/), [@StatalieT](https://twitter.com/StatalieT), :sun_with_face: 
- Nina Di Cara, PhD Student, University of Bristol, [ninadicara](https://github.com/ninadicara/), [@ninadicara](https://twitter.com/ninadicara), :writing_hand:
- Huw Day, Maths PhDoer, Bristol, [@disco_huw]
- Paul Lee, investor @pclee27
- Robin Dasler, research software product manager on hiatus, [daslerr](https://github.com/daslerr)
- Kamilla Wells, Citizen Developer, [Kamilla Wells](https://www.linkedin.com/in/kamilla-wells/)
- Miranda Mowbray, honorary lecturer, [mirandamowbray](https://www.linkedin.com/in/mirandamowbray)

## Discussion
Each week, we split into breakout rooms of 4-6 people to discuss the material. 
Please make space for one another to talk - keep your eyes open :eyes: for people with their hands up :hand: and invite them to talk.

As always we have provided some discussion points to get the conversation moving, but feel free to discuss anything relating to the materials!

::: info
### :information_source:  Notes on writing
#### Writing things down is optional

The following are all good options:
- :heavy_check_mark: Writing some notes in here as you discuss.
- :heavy_check_mark: Writing some notes in here up to a week after the discussion at any time.
- :heavy_check_mark: Not writing any notes in here at any time.

#### What to write
Suggestions for what to write down (if you want to):
- Any interesting quotes from the discussion
- Links to other material that came up in the discussion
- Parts of the reading material that you felt particularly strongly about
:::

### Discussion

#### Suggested Questions

- Q1: Denton talks about the 'view from nowhere' as a "neutral" perspective of research, and specifically data annotation. If you were building a new dataset right now, what could you do, or what have you done previously, to address this?
- Q2: Denton discusses the implications of biological essentialism. Many areas of research have 'controlled for' gender and race/ethnicity for a long time - is this the most useful way to understand differences between people?
- Q3: What current applications of computer vision can we think of that are currently in use? What implications might these have for people's lives?

- **Bonus Question:** What change would you like to see on the basis of this piece? Who has the power to make that change?

#### Room 1

##### Q1 
Fundamentals of good statistical practice... inclusion of underprivileged. 
A challenging question - I don't build datsets, I take was has already been compiled. Maybe a good skill for data scientists is to get more used to building bespoke datasets? Reusing pre-made datasets can smuggle in a lot of preconceptions that we aren't explicitly aware of!

Machine learning requires a mapped dataset for training, usually with a binary result. There is little to no accounting for the grey of the world if the model is built on true/false prediction accuracy. Worse, this can encourage us to think of the world in a binary way, and flatten complex concepts down into a binary. Could be relevant to think about how to change machine learning inputs/outputs to move away from boiling down the world in this way. 

What's the dataset going to be used for? and for whom? Then include them, not just in the dataset, but even in the design of the collection methods.

Good to think about the potential applications of the dataset - if we want to make recommendations on how to adjust controllable parameters, is it better to just measure these controllable parameters (e.g. amount of money provided as benefits) and exclude uncontrollable parameters (e.g. gender and race).

Kept coming back to fundamental problems of epistemology and perception - these problems are not necessarily exclusive to data science and machine learning, they crop up everywhere in science! We need to be aware that machine learning is the systematisation of (flawed) human perception and understanding.

##### Q2 

Discussion on variables... what are the actual relevant/useful characteristics.

Asking on gender (to ask for potential pregnancy in medical setting), instead of asking are you potentially pregnant. We need to think critically about the variable we want to know about, and separate that from variables that we assume are related/correlated. If we use these "pseudo variables" instead, we may end up encoding our own biases and assumptions in the model without realising.

How on earth can we account for race, when racial identity is socially constructed? Example: If we consider a model that tries to visually identify race, it can only (at best!) determine whether someone *appears* to be of a particular race - people can visually "pass" as a race other than the one they identify as, and this is the kind of info that visual models are fundamentally unable to understand.

Only so many boxes to select from, need to include 'Other' and/or 'Don't Know'. Machine learning can trick us into thinking that there are a finite number of discrete answers to a question!

##### Q3 

Traffic management, 'social platform for women' (phrenology in disguise), medical diagnosis of scans... are we even completely convinced on the accuracy of fingerprinting?

Generally unconvinced about the efficacy of such models, and *especially* unconvinced about models that try to visually obtain data about socially constructed concepts such as race and gender. Again, we come back to systematising human limitations - these concepts aren't necessarily neat categories that we can all easily visually understand!

##### Bonus question
Comment from Kamilla: I've added to my paper thanks to this video - lets move beyond having good intentions and look at our impact.

##### Misc

#### Room 2

##### Q1
- Let's be honest, it's not possible to be in the mythical view from nowhere.
- Example of information beyond the apparent source data: assuming an underlying biophyscal parameter
- Sometimes there is a good reason to do this (similar to anonymisation) - you can't go back to the source. Sometimes it's socially constructed wasps.
- Include people in data collection that understand and have different perspectives.
- Very detailed methods section: say where view is from since it's not from nowhere.
- Creating data sets for specific purposes rather than for anything (for personal data especially).
- Long-standing data sets, that everyone is still using: for benchmarking purposes. Everyone's forgotten the provenance and how it was made: documenting that would help us understand our lack of neutrality.
- It's difficult to get people to publish their data because it's a lot of work, or it was done by a grad student who has left, etc.
- There is a view that a view from nowhere actually exists. Disciplinary research practice wise, computer science is completely separate from the social sciences. Anthropologists and ethnogrophers have understood that you can't have a viewpointless view. 
- You're so far removed from the problem as a computer scientist: it's a maths problem. 
    - Be reminded: the data is people.
    - That's not incentivised because user personas aren't easy to compare % accuracy with.
- Solution: forcing interdisciplinarity?

> In the days when Sussman was a novice, Minsky once came to him as he sat hacking at the PDP-6.
>     "What are you doing?", asked Minsky.
>     "I am training a randomly wired neural net to play Tic-tac-toe", Sussman replied.
>     "Why is the net wired randomly?", asked Minsky.
>     "I do not want it to have any preconceptions of how to play", Sussman said.
>     Minsky then shut his eyes.
>     "Why do you close your eyes?" Sussman asked his teacher.
>     "So that the room will be empty."
>     At that moment, Sussman was enlightened.

Interdisciplinary resources:
- ‘Cadavre exquise’ - exquisite corpse: collective assembly of an output https://en.wikipedia.org/wiki/Exquisite_corpse
- http://www.bristol.ac.uk/brigstow/resources/engagedbeing/

##### Q2
Dataset design as one possible alternative.

We're trying to do things for good, so why would anyone want to use it for bad (oblivious/clueless).

There's a big difference between saying "We should collect this data and then control for it" and "therefore we can build a gaydar predictor"

More constrained problems, but that aren't just for rich white people?

We maybe need more MIPs (model intercomparison projects), like in climate science.
Or groups of scientists around the world working repeating the same kind of research.
Kind of a transfer learning problem


##### Q3

##### Bonus question

##### Misc

#### Room 3
##### Q1
(Initial Notes by Huw)
- Important to consider what is the overarching goal of the field. Is it to recognise things better or to abandon certain topics? 
- It depends on the application. Annotating data, what is it useful for? What should it be useful for?
- Publishing who your annatator(s) are. Their demographics, what instructions you gave them etc.
- It's rare to use your own data, typically you use what other people have collected. It helps to be clear about your secondary sources.
- Potentially sharing applications of the data back to the primary sources. This can be slower and more restrictive in your applications. Limited by scale of data sets.
- Is there something special about computer science research which creates distance between the data and the subjects of the data?
- Difference between liability for software and enforcing industry standards (such as for doctors and lawyers) on anyone who writes code.
- Perhaps analogous to first aid vs surgery.
- Book recommendation: "Sorting Things Out", Geoffrey Bowker 
- When do linguistic differences come in? Perhaps in an Italian data set, a higher % of men would be described as "bello" (beautiful), as that's more common than describing men as beautiful in English.
- Think about the governance/regulations are around the data set and business model around it. Don't think about good annotation practice in isolation.

##### Q2
- Perhaps we should be more humble in our claims in research. Scientists/public have to be more hesitant about concluding on big generalising "truths".
- This is difficult to work against in the competitive world of academia. 
- Another danger is that the industry might conclude from the idea that findings from a data set on one set of people might not generalize to a different people, that what's necessary is to collect data on absolutely everyone; potential privacy issues.
- A really interesting paper on controlling for gender: "This whole thing smacks of gender: algorithmic exclusion in bioimpedance-based body composition analysis", 
Kendra Albert & Maggie Delano https://arxiv.org/abs/2101.08325 FAccT 2021
- It would be good for some applicationsto control for socioeconomic status (not really relevant for computer vision).
- Stereotypes can sometimes be useful. You could give different results for an image search depending on the demographics of who is searching (e.g. show non-Western bridegroom images to a non-Western searcher) but there's a potential problem with filter bubbles.
 

##### Q3
- https://www.nesta.org.uk/feature/eight-ways-councils-are-using-data-create-better-services/damp-sensing-frogs/
- Communication between data handlers and hands on labourers is important.
Applications of computer vision with positive outcomes:
- When you deposit a cheque, computer vision is used to recognise how much the cheque is for. 
- Autonomous vehicles. 
- Industrial robots looking for defects.
- Harvesting.
- Communication between data handlers and hands on labourers is important.
- Automated heat control.
- Radiology (interpreting results).
- Smart phone authetication (potential for misuse though).
- Home medical monitoring.
- Online shopping for glasses/clothes.

Bad ones:
- Advertising technologies.
- Military applications.
- All technologies can be used for good and ill, the trouble is balancing that.


- Recommended talk by Peter Flach: "Computer Says I don't know" 


##### Bonus question

##### Misc


## After this session
You have a week to add anything else that you'd like to to this document. 
After that, we'll try to make this document a little more cohesive, then we'll send a link around to the write up of the discussion in the next mailing list email.

## Feedback on the format
Please feel free to leave us some notes below on how the discussion group went for you this time, positive or negative, and any suggestions to improve (you can always [email us]() instead). 
We do read these and make changes :sparkles: 

* Suggestion here
* Another suggestion here