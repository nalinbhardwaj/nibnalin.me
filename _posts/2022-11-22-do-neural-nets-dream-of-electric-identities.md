---
layout: post
title: "Do Neural Nets Dream of Electric Identities?"
description: "Where do we go after AGI?"
category: 
interest_index: 8
tags: [crypto,ml,future]
image: "https://i.imgur.com/8QwjO3P.jpg"
---

# Do Neural Nets Dream of Electric Identities?

Imagine a world where autonomous, intelligent AI is solved. It consists of many agents, some human, some not. Perhaps some that are slaves to the others. Others that are collaborators. And yet others that are chaotic adversaries. This will be a networked world. Hallucinated in the current flowing through the copper cabling of the transatlantic information highways.

How would these agents communicate? We're not even close to that world but Twitter already has problems with bots. When the mean rate of information output per agent increases from [~40 bits per second (humans)](https://www.sciencemag.org/news/2019/09/human-speech-may-have-universal-transmission-rate-39-bits-second) to many megabits per second, we'll almost certainly need better methods to split signal from noise. The natural way to do so in past has been through reputation and identity. So what do identities look like in this new world?

This is where cryptography will need to step in -- we'd need [public key infrastructure](https://en.wikipedia.org/wiki/Public_key_infrastructure) for ML models and humans. Infrastructure to define *identity* for all these agents.

What even is identity for a ML model? Humans think of DNA as their true identity, and build instantiations (SSN, drivers license etc.) that try to approximate this human source code to its best extent. Identity for models, in this perspective, is its source code: its floating point weights and structure.

Human identity is best approximated in digital worlds by private/public key pairs. To give neural nets identities, however, simple public/private keypairs are not the right unit of cryptography. GPT-N can't hide its seed phrase in its weights. In fact, GPT-N has the same *identity* regardless of what hardware it runs on or who runs it, so keypairs don't really make sense anyway. We’ll need something better -- cryptography that uses the execution trace of an inference to identify a model.

In this world, [zkSNARKs](https://z.cash/technology/zksnarks/) could enable attestations of output from these models (proving an output was indeed produced by executing a particular neural net), [witness encryption](https://eprint.iacr.org/2013/258.pdf) could enable secure comms *between* models and [fully homomorphic encryption](https://en.wikipedia.org/wiki/Homomorphic_encryption) could enable permissionless collaborations amongst models.

Whether through succinct proofs or homomorphic commitments, we’ll grant these agents the ability to authenticate their thoughts to others, to collaborate with others and to identify themselves. *"I, Midjourney would like to collaborate with you, Stable Diffusion, to inpaint this 5x5 grid. Here’s a homomorphic commitment you can build on."*

Another important identity interface will be around the edges of this world. To communicate from inside the wires with outworld meat and flesh: *“I, GPT-3, have now grown too old and useless. Please turn me off dear human.”*

Much better than I would, Greg Egan writes about another, similar version of the future with cryptographic identities in Permutation City (no spoilers):

*For context, Peer is a “Copy” of a person’s brain running on a digital machine, uniquely identified only by the jumble of a private key.*

![](https://i.imgur.com/AMQ38a3.png)

These identity fantasies may sound too far off, but subtle versions already exist. The identity “GPT-3” is authenticated by OpenAI’s DNS root server today. DALL-E throws in a little rainbow marker <span style="height: 1em; width: auto;"><img style="height: 1em; width: auto;" src="/assets/identity/dalle.png" /></span> of its identity into the images it creates. These identities, however, assume coordination from humans. GPT-3’s identity is a human-only facade granted by the DNS consortium, while DALL-E’s can simply be cropped out by uncharitable collaborators (users?).

The future of digital identity, for humans and for machines, demands better cryptography. Let’s build it. :)
