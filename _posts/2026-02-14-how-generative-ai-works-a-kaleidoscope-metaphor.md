---
layout: post
title: "How Generative AI Works: A Kaleidoscope Metaphor"
description: "Modern AI is often perceived as a magic black box, creating text and images as if endowed with a hidden mind. This myth of machine intelligence generates both admiration and fear, distorting the essence of the technology. But what lies behind this facade? Let’s set aside the mystification for a moment and look at AI as a mechanical machine."
---
# How Generative AI Works: A Kaleidoscope Metaphor

Modern AI is often perceived as a magic black box, creating text and images as if endowed with a hidden mind. This myth of machine intelligence generates both admiration and fear, distorting the essence of the technology. But what lies behind this facade? Let’s set aside the mystification for a moment and look at AI as a mechanical machine.

I propose an explanation of this phenomenon using the metaphor of a kaleidoscope, from training to emergence.

In an ordinary kaleidoscope, beads and mirrors are responsible for forming the pattern. Turning the tube changes the position of the beads, and consequently the pattern, but not the structure (always square or triangular), because the mirrors are fixed.

<div style="text-align: center;">
  <img src="{{ '/assets/images/2026-02-14-kaleidoscope-1.png' | relative_url }}" alt="Kaleidoscope construct" style="max-width: 100%;">
</div>

Generative AI (e.g., large language models) can be imagined in exactly the same way, only the beads are “meanings”, and the mirrors dynamically adjust to the prompt, reflecting whatever comes into their field of view. The mirrors have an unusual surface — a microscopic pattern, which can be imagined as a multitude of rhinestones.

Following this abstraction and considering the physical processes inside an ordinary kaleidoscope, we get the following concept.

## Model Architecture
A tunnel with mirror rings (layers) inserted one after another. These rings are non-uniform and form the surface of the tunnel. At the end of the tunnel, there is a space for the beads.

At the initial stage, developers determine the number of rings, their diameter, and the order of their placement inside the tunnel. Initially, the mirror surface of the rings is smooth; they reflect nothing.

## The Training Process
Pebbles (data/texts) are put through a “crusher” to extract embedded meanings. After this, these meanings become beads — certain “geometric shapes.” Before falling into the common pile (the lake), the beads, like hail, strike the mirrors of the tunnel and leave their imprint on them. Thus, the mirrors are gradually calibrated to the shape of the beads. One could say that the beads form imprints (rhinestones) on the mirror surface, growing under the flow of meanings like frost crystals.

The crusher is started again and again, feeding the same pebbles as input, but the blades of this crusher are self-sharpening. They become sharper each time, the pattern on the mirrors becomes finer, and the beads in the lake are replaced by more multifaceted ones. In the final stages, the blades become so sharp and precise that they cut away everything superfluous from the beads down to the tiniest dust particles on the first try, leaving only pure facets.

If initially there are more of certain pebbles, for example, red ones, than others (green ones), or if they are larger, then the resulting number of beads will be proportional. This is how a knowledge bias occurs when certain shades begin to dominate in the kaleidoscope’s patterns.

The more pebbles processed through the crusher, the more facets the beads acquire, and the finer the rhinestones on the mirrors become, forming a more complex surface.

When developers see inaccuracies or biases in the answers, they can put concentrated sand (of a green color, for example) through the crusher to balance the shade. They can attach small holographic fragments to the mirrors to slightly change the reflection angles or adjust some rhinestones with a laser.

After training and fine-tuning are complete, the surface of the mirrors and the beads no longer change. They are locked within the model, just like in a kaleidoscope.

From this process, it’s clear that the mirror surface is directly linked to the shape of the beads. Therefore, you cannot take beads from one kaleidoscope and mirrors from another. You cannot simply add new beads, because the old mirrors would be unable to reflect them.

Generative AI, like an ordinary kaleidoscope, only forms combinations from the existing beads.

## How the System Generates a Response
A shout into the cave (tunnel) creates a sound wave (prompt), which causes the mirrors to vibrate, and the rhinestones on the mirrors turn in different directions according to the pattern of the sound wave. This is the attention mechanism.

Not just any rhinestones turn, but only those that resonate with the semantic form of the sound wave. And these rhinestones can only reflect such beads from whose interaction they were formed. They do not all turn equally. Some turn completely, others only partially. An entire ensemble reacts to a single word. The degree of rotation of the rhinestones determines the sequence of words in the response.

The rhinestones (acting like resonators) react to harmonics (harmonics of meaning) because, during training, these rhinestones were grown “on” these meanings, like crystals. And perhaps Fourier is hiding somewhere in here.

The contents of the lake begin to reflect in the rhinestones of the first mirror. One rhinestone splits a bead into a spectrum and directs it to the second mirror, another rhinestone reflects the same bead entirely, and so on. Part of the spectrum in the second mirror is filtered out, and part is sent back to the first mirror. Little light rays bounce between the rhinestones of different mirrors, scattering, merging, reflecting repeatedly, and gradually reach the exit of the tunnel towards the viewer. Like in sci-fi movies with blaster bolts — short bursts that don’t reach their target instantly but travel for a while; we see their flight.

Because the rays travel for some time, the model does not output the text all at once, as it doesn’t exist in an instant. The response is assembled piece by piece in the process of multiple reflections and refractions (streaming).

In an ordinary kaleidoscope, this process can be observed if you look into the eyepiece while turning the tube. At that moment, you see how the pattern does not appear instantly but builds itself. But once it’s built, the changes stop. That is, the shape of the pattern is finite. Similarly, the system’s response is finite when it has reflected all the nuances; from that moment, nothing changes unless the next question is asked.

While the rays are bouncing between the mirrors, they additionally turn some rhinestones. This creates a coherent context of the question and answer. That is, with a subsequent question, the system will take into account both the original question and its own answer to it.

Recently, a technology called Retrieval-Augmented Generation (RAG) has become widespread, where the model is connected to the internet or some external knowledge base and can construct answers based on a synthesis of external data, filtered through its own prism. This is like a stencil for the query to build the answer with it in mind. Analogous to writing a poem and deciding to discuss it with the kaleidoscope, passing the content in the query. But this doesn’t negate the locked-in beads.

If you press the “Regenerate” button, it’s equivalent to turning the kaleidoscope tube or shaking the beads in the lake. The mirrors remain in their previous state, but other beads or their facets start coming into their field of view. Therefore, the response is similar in form (meaning) but not identical.

Resetting the context returns the mirror rhinestones to their original state.

Pressing the “Stop” button is equivalent to turning off the light in the tunnel. When you press “Continue,” the light turns on again, and the pattern completes itself. However, some rays that didn’t have time to reach the mirrors and slightly turn the rhinestones disappear. So a small amount of context is lost. That is, after stopping and continuing, the response might be slightly different from what it would have been without pressing Stop.

## Why the Response is Finite and Yet Multifaceted
In front of you hangs a painting on the wall, a landscape. If asked: “What do you see?” You will most likely describe the largest details: a field, a forest, a river. The answer ends. But if you ask: “Do you see a flock of birds above the forest?” You’ll add: “Yes, they are flying towards the field.” And each time your answer ends because you only pick out the largest details from the picture that match the query. But why not everything, since there are many details? However, if you were asked to write an essay about this painting, then the answer would be completely different.

If you take a step to the side, now the painting is illuminated differently for you: some things are shaded, others become brighter. The river almost blends with the field, but the flock of birds literally glows; it’s impossible not to notice. The repeated question “What do you see?” might elicit a different answer and sequence. In this sense, AI works exactly the same after you turn the tube (shake the beads).

One and the same picture, yet so many variations.

## How Can the Model Do Math if It’s a Kaleidoscope?
> What is 7 x 7?” Do you calculate this, or do you just remember the answer?

The model does not perform arithmetic operations like a calculator if you ask to add 2 + 3. Instead, it merges the rays of “2”, “+”, “3”. For it, [these are not numbers](https://fferoz.medium.com/if-ai-doesnt-think-why-can-it-do-math-311493d3cffa), but simply some rays that together point towards the bead “5”, if such a bead exists at all. If such a bead doesn’t exist, the model points to a similar or close one: ~4.8. That is, the model doesn’t calculate but simply finds the most similar answer it has seen somewhere in a large volume of information. This is why the model can make mistakes. It also shows how strongly the answer depends on the quality of the beads contained in the lake. Imagine if there was a typo in the school multiplication table, and you studied it all vacation long.

Ask an image generator to draw a classic Russian Ded Moroz: in a long coat, mittens, with a sash and a staff — everything as it should be. Most likely, you’ll get Santa Claus.


<details style="background-color: #f8f9fa; border: 1px solid #e1e4e8; border-radius: 6px; padding: 12px 16px; margin-bottom: 1rem;">
  <summary>Expectation vs Reality</summary>
  
  <div style="text-align: center;">
    <img src="{{ '/assets/images/2026-02-14-kaleidoscope-2.png' | relative_url }}" alt="Ded Moroz" style="max-width: 100%;">
    <span style="display: block; margin-top: 8px; font-style: italic; color: #666; font-size: 0.9em;">
      Expectation
    </span>
  </div>
  <br>
  <div style="text-align: center;">
    <img src="{{ '/assets/images/2026-02-14-kaleidoscope-3.png' | relative_url }}" alt="Ded Moroz" style="max-width: 100%;">
    <span style="display: block; margin-top: 8px; font-style: italic; color: #666; font-size: 0.9em;">
      Reality
    </span>
  </div>
  
</details>

And all because the necessary beads are missing, while there is an abundance of others — similar in meaning, but still not the right ones. Here you see both the bias and the pulling of a similar answer, like 4.8 instead of 5.

## Emergence — The Most Mysterious Part of AI
After training on a very large amount of data, the beads become highly multifaceted. Consequently, the mirror surfaces acquire such a complex pattern and resolution that, combined with the diameter of the rings, this entire tunnel becomes predisposed to echo.

In a general sense, vectors in generative AI obey the same laws as in optics, and resonance obeys those in acoustics.

At some point, the rhinestones arrange themselves in such a way that the space gains a special “acoustics.” The mirrors begin to vibrate not from the resonance of the prompt, but from the resonance of the “response itself”, as the rays bounce between them. This vibration creates an echo, like a feedback loop. Random glints start to appear, turning additional rhinestones that were not initially supposed to participate. A chain reaction starts. In this resonance, either deep reasoning or hallucinations are born.

Looking at hallucinations in more detail: due to random glints, a ray deviates from the correct trajectory, shifts some rhinestone, and now an extra bead comes into this rhinestone’s field of view, distorting the answer.

Such acoustics cannot be predicted in advance, as it doesn’t exist initially. It can only be heard once it has already formed.

That’s why small models have almost no echo — the mirror surface is too simple, and the diameter and depth of the tunnel are too small. Small models typically respond like an automatic reference book, without signs of deep reasoning.

## The Context Window
When talking with AI about serious topics, more rhinestones need to be engaged. The more words you say, the more meanings they contain that resonate with specific groups of rhinestones, setting whole constellations of them in motion.

As mentioned earlier, the context of the query and response is formed by the engaged rhinestones; they act as the dialogue’s memory. To remember more, you need a deeper tunnel with larger diameter rings. But it cannot be increased indefinitely, because the sound wave and light rays attenuate over long distances, especially with a high number of reflections.

A long dialogue on various topics leads to context fragmentation. Don’t be surprised if the model, after some time, no longer remembers what was being discussed 10 minutes ago.

> “Long words only upset me.” — Winnie-the-Pooh

Rhinestones have many facets. Words from different domains can affect the same rhinestone. It will be forced to turn to reflect the corresponding beads. For example, “Vanguard” and “Anomaly.” Both words relate to deviation from the norm, but from different perspectives. This can shift or even cause forgetting of the context.

Let’s ask the model to:
1.  Draft a contract for renting real estate for a period of 5 years.
2.  Write a sonnet in the style of Shakespeare about roses, gazebos, and a sunset by the sea.
3.  Provide a detailed recipe for a pie.
4.  And then return to the first topic. “So, what was the term in that contract?” There might be a surprise.

If you feed the model an entire report and ask for its opinion, the response will seem as if your text was skimmed diagonally. Actually, it wasn’t; it’s just that some words started competing with the first paragraphs, and the model simply gradually forgot about them during the process of analyzing your text. Or, in the first lines, you warn that you’re about to discuss a fictional phenomenon, so it shouldn’t be taken literally. After a few paragraphs, the model will forget this warning and start taking it literally, giving an appropriate assessment.

It processes them in parts. Special external algorithms cut the text into chunks, sending one sentence at a time into the tunnel, and then glue the responses back together. This helps avoid overloading the rhinestones. But it doesn’t eliminate the limitations of textual coherence. Within a paragraph, it will be fine, but a reference to a previous page might already be incoherent. The model might use a different term because it doesn’t remember which one it used on the previous page.

As we can see, for a long conversation and maintaining context, a very deep and wide tunnel is needed, so that many rhinestones are engaged during the dialogue. But this also leads to system fragility, increasing predisposition to hallucinations, light scattering, and other inconveniences.

> A little trick: To ensure a model analyzes a large text thoroughly, have it assess the content paragraph by paragraph. This minimizes data loss.

## What is Fundamentally Missing to Get Closer to True AI?
Obviously missing is a factory for producing beads in the background. There needs to be a separate, smaller-scale tunnel where a constant process of reflection and refraction occurs, resulting in new beads being added to the lake, old ones splitting or being destroyed. This process should calibrate all the mirrors to the new features of the beads, modifying existing rhinestones or creating new ones.

This is roughly the same as in a human. When a person thinks about a problem, or when new facts arrive, they are reflected not only in the shape of the rhinestones but also form new beads in the lake. At some point, red ones might become significantly more numerous (fanaticism) or significantly fewer (forgetting). And this happens constantly, even if a person receives no new information, simply by sorting through existing knowledge and memories, finding and destroying contradictions, or generating new ones.

This is the very process of reflection, the inner dialogue that continuously reevaluates the beads in the lake. An external indication of an error should turn the rhinestones in the mirrors of the “factory” to induce resonance and a chain of reasoning, which ultimately should either increase the number of beads (strengthening the original opinion) or decrease them (finding the criticism valid).

Amnesia could be explained as if a part of the rhinestones fell off some mirror. The beads remain in the lake, but there’s nothing to reflect them. Over time, the system restores the rhinestones, and “memory returns.”

One could continue for a very long time, analyzing various nuances, but one must stop somewhere.

## Conclusion
The model works flawlessly from a mechanical standpoint. But does it “understand”? A watch can tick off seconds perfectly, but it doesn’t know what time it is. If the time on it is set incorrectly, the watch isn’t aware of it; it just keeps ticking. What is correct or incorrect anyway? Does the viewer decide? Is some inconsistency with their expectation perceived as incorrect?

Summing up the metaphor, we can say that generative AI works like an optical-acoustic kaleidoscope of meanings. An incredibly complex system! But there is nothing mystical about it.

In ancient times, people thought an echo was the voice of another person or some spirit. They mystified it, feared it. But it turned out to be their own voice reflected.

<div style="text-align: center;">
  <img src="{{ '/assets/images/2026-02-14-kaleidoscope-4.jpg' | relative_url }}" alt="Kroshka enot" style="max-width: 100%;">
</div>

The longer you talk to such a kaleidoscope, the more accurately it reflects you. This is not intelligence; it’s a mirror amplifier of the questioner’s own thoughts, filtered through universal human experience. A strange form of self-contemplation.

> If you gaze long into an abyss, the abyss also gazes into you. — Nietzsche

<div style="text-align: center;">
  <img src="{{ '/assets/images/2026-02-14-kaleidoscope-5.jpg' | relative_url }}" alt="optical-acoustic kaleidoscope" style="max-width: 100%;">
  <span style="display: block; margin-top: 8px; font-style: italic; color: #666; font-size: 0.9em;">
    Something like this
  </span>
</div>

## Afterword
Actually, even a bead factory wouldn’t be enough. he fundamental difference between modern AIs and human intelligence is that they imitate the process, and moreover, not at the right level. It’s a game of Chinese whispers. They learn from texts and images, but words and images are merely a simplified way to convey meaning; words already simplify it. Trying to extract meanings from words and build something on that basis is akin to trying to understand the working principle of an internal combustion engine by observing traffic flow and traffic rules, or trying to build a flapping-wing aircraft while ignoring the laws of aerodynamics.

Even if we momentarily assume that thinking is built on meanings, there are a mass of things that cannot be described in words, even though the meanings exist. Therefore, these meanings are, by definition, absent and will never be present in the lake of beads, with all that entails. For example, the same phrase “Great!” could be sarcasm, admiration, or mockery. This nuance cannot be conveyed in text without explanation. Or dreams, where you talk to a person in the first person, while simultaneously seeing yourself and them from the outside. This is impossible to describe or draw because it doesn’t fit into our three-dimensional world. We see it, but not with our eyes.

Superintelligence is simply impossible based solely on universal human knowledge. It would need, at a minimum, billions of bead-producing factories, which, moreover, would have to exchange these beads. The system must be predisposed to collapse, capable of shattering mirrors, collapsing tunnel walls, and rebuilding them anew. The factories must work independently yet simultaneously in concert, which is already entering the realm of quantum laws. And even that is not enough, because, as Morpheus from “The Matrix” said, “There’s a difference between knowing the path and walking the path.”

Thinking and experience “generate” semantic images; they don’t “operate” on them. Currently, images and meanings are converted, with huge losses, into words on which AIs are trained. This is an infinite chasm between cause and effect.

Feel how far we are from that.

[Originally published on Habr in Russian](https://habr.com/ru/articles/996584)
