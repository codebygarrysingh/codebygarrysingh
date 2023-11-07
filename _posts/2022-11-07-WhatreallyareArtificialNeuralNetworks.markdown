---
layout: post
title:  "What really are Artificial Neural Networks: A beginner’s guide to a Single Neural Node"
date:   2023-11-07
categories: 
  - "Artificial Neural Networks"
  - "Machine Learning"
  - "Artificial Intelligence"
author: Garry Singh
---
<div class="summary">
     <span class="fas fa-robot icon"><b> In the Brief</b></span>
  <p>
    Artificial Neural Networks (ANNs) are digital doppelgangers of the human brain. Just as the human brain processes information and makes decisions, ANNs are designed to do the same, computational fashion. The magic lies in the mimicry.

At the heart of ANNs are the “neurons” or what is called a “Neural Node” in machine learning world. It’s small computational unit that function like their biological counterparts.

These Neural Nodes are organized in layers, just like neurons in different regions of the human brain, each with its unique role in information processing.
  </p>
</div>
<br>
When I initially started learning machine learning code, little did I know that I was about to embark on an odyssey through a realm where words like “neural networks,” “backpropagation,” and “activation functions” would be as common as ABC.

Artificial Intelligence, the field that’s reshaping our world, comes with its own glossary of terms that can make your head spin.

There have been overwhelmingly mouthful of buzz words related to AI that anyone thinking of jumping on this new wave of innovation might feel like they’ve stepped into a tech-driven buzzword bingo game.

But you don’t need to feel over exhausted with these, although I have learned this the hard way, I am on a mission to make it easier and fun for for you to understand it.

Before we get into the dazzling world of Artificial Neural Networks, let me offer a friendly advisory note for our readers. You don’t need to be a programming guru, an engineering wizard, or a computer sorcerer. In fact, the analogy of this topic is drawn from very functioning of human brains.

So if you are the curious one craving the secret sauce to sound smarter during the office coffee break, in the schoolyard, or around the family dinner table, then hop on the train for the journey ahead.

<br>

## <b>Let’s understand inner workings of our biological brains</b>
Before we dive headfirst into understanding Artificial Neural Networks (ANN), Let me present to you the inner workings of the human brain.

Imagine your brain to be a digital library of books, like a Kindle Book or if you’re still old school (not that its out of fashion) you may consider a physical library. The idea is very simple that every book holds piece of information and has a certain start and a conclusion.

![Book Library](/assets/images/whatreallyareann_img1.png)

Now some books may contain independent topics which have independent conclusions and some books could either be about series of a topic in chronological order where every conclusion is a beginning for another title.

This is a loosely laid out analogy of how our brains work. Our brain has something equivalent to books in a library called Neurons. Neurons are fundamental building blocks of the brain that take information in and transmit conclusions.

The reason I said loosely in the conversation is because there is a slight twist to how Neurons process information and computations, contrary to how books store static bit of information.

Neurons are like rewritable books that only takes in information for processing conclusions or more or less like erasing and rewriting their content.

These dynamic “neural books” adapt, change, and communicate with one another, creating the magnificent symphony of our thoughts, memories, and actions.

<b><u>Fun Fact:</u></b> The number of neurons in an average human brain is estimated to be around 86 billion. There are hundreds of millions of neurons in the stomach, so when next time someone says they have a “Gut Feeling”, they’re really talking about conclusions from “neural books” in their Stomach.

Now, here’s a fascinating question you might ask: how does information travel from one “neural book” to another in the brain?

Well, the answer lies in neurotransmitters.

Think of neurotransmitters as the couriers of information, akin to signals traveling from one neuron to another.

To illustrate this concept further, imagine our “neural books” as high-tech, Bluetooth-enabled devices. In this analogy, neurotransmitters serve as the Bluetooth signal, transferring knowledge from one “book” (neuron) to the next.

Now, when these signals traverse the space between books, think of it as if they were traveling through the air, much like your Bluetooth signal. In the brain, this vital pathway is known as a synapse.


Consider the synapse as a link or bridge that facilitates the journey of neurotransmitter chemicals between two neighboring neurons, ensuring the smooth transmission of information.

Now that we have some basic idea about inner workings of the brain, with a drumroll, unravel what ANNs really are!!

<br>

## <b>What really are Artificial Neural Networks?</b>
Picture below is the first thing that probably comes to anyone’s mind thinking about Artificial Neural Networks, the reality is as fascinating as it seems, there’s more to it than meets the eye.

![Neural Network Potray](/assets/images/whatreallyareann_img2.png)

Artificial Neural Networks (ANNs) are digital doppelgangers of the human brain. Just as the human brain processes information and makes decisions, ANNs are designed to do the same, computational fashion. The magic lies in the mimicry.

At the heart of ANNs are the “neurons” or what is called a “Neural Node” in machine learning world. It’s small computational unit that function like their biological counterparts.

These Neural Nodes are organized in layers, just like neurons in different regions of the human brain, each with its unique role in information processing.

Now just imagine how by looking at a person we can associate an identity with the person, this is because our eyes send visual signals to brain and these signals are deciphered by complex web of neurons to find meaning and association.

Similarly, advanced ANNs can perform face recognition from images/videos by reading and processing millions of pixels of image data into layers of neural nodes to produce an identity association.

While ANNs are inspired by the brain’s structure, it’s essential to note that they are not models of human consciousness or brain function in a comprehensive sense. ANNs primarily focus on data processing and pattern recognition, aiming to replicate certain aspects of neural function.

Now, while Artificial Neural Networks offer a wide array of components and functionalities, let’s stay focused on our agenda and delve into the inner workings by examining the operations of a single Neural Node.

Let’s examine a Single Neural Node
Since we already covered inner workings of the brain earlier, you must be thinking the operations of a single artificial neural node shouldn't be any different than a single biological neuron model, if so, then yes, you are absolutely correct!!

Now before you get too excited and give yourself a pat on the back, let’s cover some terms that are more relevant to Machine Learning world (since you want to sound like a AI/ML geek not a neurologist).

Now don’t be sad yet, these terms are not any different from what we have already discussed and you can draw a clear symphony.

<br>

## <b>Neural Node has following components</b>

-- <b>Inputs:</b> This is any standard input data, just imagine this as input to your “Neural Books”, an example of input can look like pixel intensity in case of image processing.

-- <b>Computation Function:</b> This is where your take the inputs and perform computation/calculations, like we saw in Neurons, this is also called as Aggregation function in ML world.

-- <b>Decision Function (aka Activation Function):</b> Here, the neural node processes the input, makes decisions or predictions, and correlates to the conclusion of a “Neural Book.” For example, It determines how close the input pixel is to a specific intensity.

-- <b>Output:</b> The output is the signal sent to the next layer or neural node for further processing. It’s essential to note that in many computational models, the output is mapped to a binary scale, typically 0 or 1, representing the probability after each neural node’s computation.

Now there is more to the simplified description given above, concepts like training weights and biases. However to not get your brains fuzzy with all the nitty gritty, this should be a good starting point to build your understanding.

Now, just to put things into perspective, here is what a standard Artificial Neural Network look like, not too different from our imagination right…

![Artificial Neural Network](/assets/images/whatreallyareann_img3.png)

Just think of each of those circles to be your Neural Nodes that are taking inputs, doing necessary computations and sending decisive outputs to next node.

<br>

## <b>One last thing, let’s see how it works</b>

Now if you have made this far, kudos👏 to you, Good Job. I promise this is end of our quest to understand ANNs.

The code you see below is pseudo code or in simpler words, presented in a conversational tone, showcasing how training a single node looks.
```python
# Pseudocode for a Single Neural Node

# Step 1: Receive Input
input_data = get_input_data()  # Get data, like pixel intensity in an image

# Step 2: Perform Computation
# Don't worry about details, just understand this is your computation function
weighted_sum = 0
for each input_value in input_data:
    weight = get_weight()  # Retrieve the weight associated with the input
    weighted_value = input_value * weight 
    # Accumulate the result of computation
    weighted_sum = weighted_sum + weighted_value 

# Step 3: Make a Decision
# Threshold is likelihood that the input contributes to a particular outcome
activation_threshold = get_activation_threshold() 
if weighted_sum >= activation_threshold:
    decision = 1  # The decision is positive or "Yes"
else:
    decision = 0  # The decision is negative or "No"

# Step 4: Send Output
send_output_to_next_node(decision)  # Pass the decision to the next neural node

# End of the Neural Node Operations
```
I hope this has put things into perspective and given you enough information to crack those initial conversations with your friends, colleagues or even family with sufficient context.

I will cover more in detail about practical implementations using Artificial Neural Networks and share relevant real-world practical examples in future blogs.
