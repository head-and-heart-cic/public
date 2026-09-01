# A handle on AI
**Date:** 02/09/2026

## AI as hunch dispensers

When it comes to using and governing AI, thinking in terms of “hunch dispensers” provides a much clearer vantage point than “artificial intelligence”. Generative AI dispenses hunches. Agentic AI takes things a step further by embedding one or more generative AI hunch dispensers into an automated workflow that acts on those hunches.

In abstract terms, generative AI takes a pattern (the explicit prompt) and extends it (the response) in a way that resembles a much larger pattern (training material, plus grounding and contextual material).  This resembles the way humans can take a step back and form a hunch based on their perception of the world they live in, rather than by following a line of reasoning. In practical terms, generative AI creates abstract patterns that usefully resemble actionable hunches. Put another way, we can prefix any generative AI output with “I don’t actually understand your request, but my hunch is that you are looking for an answer that looks something like…”  

## The value of hunches

Hunches are an important and often powerful tool in our lives; notably, professional expertise is a blend of knowledge and well-developed hunches that the expert judges to be sufficiently reliable to act upon.

There was a recent demonstration of the value of both human and generative AI hunches in an operation in which a surgeon used AI-generated real-time analysis of scans to help remove a brain tumour [1]. The surgeon's professional expertise could draw upon the much wider field of view provided by the AI's analysis, but ultimately it was the surgeon's assessment of these hunches that guided the scalpel. 

Hunches become valuable in exactly two ways: they can provide evidence as part of a wider analytical process used to decide how to act, as the surgeon used the AI analysis; or they can be acted upon directly when we judge them to be the most appropriate basis for deciding how to act on a particular occasion, as the surgeon used his own hunches.

## The limitations of hunches

Hunches without judgement are merely speculation. It is only when hunches are combined with reliable judgement that they become actionable expertise.

Generative AI can generate hunches, but something else needs to be used to judge whether a hunch is sufficiently reliable to act upon. If you try to use generative AI to make that judgement, you simply end up with hunches about hunches.

Whenever agentic AI acts, it is because somewhere along the line a human has judged its output to be sufficiently reliable to act upon. That judgement may have been careful or cursory. It may have been explicit or implicit. The person making it may not even realise that they have made it or have intended to make it. Nevertheless, there is always a human judgement somewhere in the chain.

If an AI guided robot were to perform brain surgery instead of a human, the hunches used to guide the scalpel in the theatre would be much the same, but the judgement of which hunches to act on would be different.  Instead of a surgeon judging hunches moment by moment in the theatre, a clinician would have effectively pre-approved whatever hunches the agentic AI acted on by scheduling the surgery.

## Hunches and calculations

In practice, agentic AI workflows almost invariably combine probabilistic hunch dispensers with calculations: deterministic processes that take an input and produce an output in a completely predictable way.

The defining characteristic of calculations is that they are predictable. This makes unpredictability one of the defining characteristics of hunches. If a decision is completely predictable, then it is a calculation rather than a hunch. The biggest challenge when deploying AI is that pre-approving unpredictable outputs is more demanding than pre-approving predictable ones.

A doctor can routinely prescribe the fitting of an insulin pump based on the expectation that the computer built into it will predictably dispense insulin according to a calculation that the doctor judges to produce actionable instructions.  Once the software and hardware used to perform the calculation have been judged to work sufficiently well, assessing the logic of the calculation is enough to justify treating the pump's output as actionable instructions.

The challenge that generative AI brings is that there is no assessable logic behind an individual hunch. Instead, we need to take into account the reliability of past hunches to meaningfully estimate the reliability of future hunches.

## The source of the hunches

We can take steps to influence the reliability of the hunches generative AI dispenses, starting with the choice of material that is used to train it.

Large Language Models (LLMs) are trained on vast amounts of general material written by people. Because widely accepted facts, common patterns, and conventional ways of expressing ideas tend to appear repeatedly throughout that material, the hunches generated by an LLM will often echo the everyday truth behind those patterns.

Small Language Models (SLMs) are trained on smaller collections of specialist material. They are tuned to echo the specialist truth behind that focused material more accurately than general-purpose LLMs, although they are less reliable outside that specialist area.

## Shaping the hunches

The full prompt sent to a generative AI system is made up of the explicit prompt that you want a response to, together with additional material intended to increase the likelihood that the response will be relevant. Typically, a user of a generative AI system controls the explicit prompt, while the developers of the system use contextual material to tie the individual response to the wider application, and grounding material to align it with relevant external information.

If you type “How do the figures in the quarterly reports for 2020 to 2024 affect this plan? Please respond with a 10-item bullet list” into a chatbot, the full prompt that is sent to the generative AI system will include:

- the text you typed, 
	
- a transcript of the conversation so far for context,

- grounding material extracted from the quarterly report files.  

The result is a hunch that looks like it could be a response from someone who has been part of the conversation and has read the quarterly reports.

## Processing the hunches

Once a hunch has been dispensed, it can be processed in an attempt to produce something more likely to be reliable enough to be actionable.

One option is to feed the hunch into another generative AI system for refinement. For example, generative AI could be used to draft a factual reply to a customer complaint. That draft could then be sent to a second generative AI system to make the tone friendlier, and the revised draft could then be sent to a third generative AI system to check it against legal requirements.

This may result in a final output sufficiently reliable to act upon in a particular context, but it does not necessarily make it more reliable in any absolute sense. The version with the friendlier tone might be less accurate than the original draft, while the more legally compliant version might be less friendly and less accurate than the first draft.

A second option is to apply calculations to the hunch. This method is commonly used when computer code is written with generative AI. The code can be tested to confirm that its syntax is valid and to look for specific programming flaws. The result is code that, although not guaranteed to do what was requested, is confirmed to meet specified standards and can be meaningfully worked with in a code editor.

The third option is to pass the hunch on to a person. Typically, they will review it and either accept or reject it. Sometimes they will amend it. Even if the person chooses to accept the hunch without reviewing it, the fact that they chose to accept it blindly is enough to make them the person who judged the hunch to be reliable enough to act upon.

The element of choice is essential. If rejecting the hunch is not a viable option for any reason (including workload), then the judgement to act upon the hunch remains upstream.

## Governing AI

I hope the idea that generative AI and agentic AI are powered by hunches will be useful as you grapple with this increasingly prevalent technology.  Before I finish, I would like to look at what treating generative AI as hunch dispensers helps clarify about Microsoft’s six principles for responsible AI use.

### Fairness

Hunches have a random component, so using AI to make decisions that could reasonably be calculated precisely introduces randomness that is potentially unfair.  Equally, they are not completely random, so when using hunches is justified, the principle of fairness demands that you take reasonable steps to ensure that the hunches your AI acts on are not unfairly biased. 

### Inclusiveness

Any use of hunches that is not inclusive is unfair, so when considering the use of hunches alone, the principle of inclusiveness demands that you pay special attention to making sure that the bias and randomness of the hunches used do not unfairly exclude anyone.   

### Reliability and Safety

The ongoing reliability of a hunch generator cannot be measured directly, only estimated from the reliability of past hunches, and it can change over time.  This makes actively monitoring the reliability of the hunches being used a matter of ongoing maintenance.

### Privacy and Security

Reliability issues are relevant to privacy and security, but another factor arises from the way hunches are shaped by adding grounding and contextual material to the explicit prompt. There is a lot of information being passed around behind the scenes, so extra care needs to be taken to ensure that sensitive information is handled appropriately.

### Transparency

One of the defining characteristics of hunches is that they are opaque. The nearest thing a person can find to a rationale for an AI-generated hunch is often an explanation of which parts of the explicit prompt, grounding material, or training material made a particular output more likely.

Transparency therefore involves being open about how AI was used, what information informed the hunches it generated, and who is accountable for judging those hunches to be actionable.

### Accountability

To avoid scapegoating, accountability needs to derive from responsibility, and responsibility needs to derive from the judgement that authorised the action, however far upstream that judgement occurred.  In practice, it is often easiest to shift the judgement downstream with an identifiable human-in-the-loop.

[1] BBC News. World-first AI-assisted brain surgery saves patient's sight. 27 August 2026. Available at: https://www.bbc.co.uk/news/articles/cjwg5n7y68xo (Accessed: 1 September 2026).

[2] Microsoft. Responsible AI Principles and Approach. Available at: https://www.microsoft.com/en-gb/ai/responsible-ai (Accessed: 1 September 2026).

Patrick Killeen  
Head and Heart CIC  
patrick@headandheart.info  
www.headandheart.info

This work is released under the MIT Licence and is available at  
https://github.com/head-and-heart-cic/public/blob/main/resources/a_handle_on/a_handle_on_ai/README.md
