**Relationship between CNNs and the human brain**

The human brain receives light from the outside world via the retina (located at the back of the human eye, see below).

![[Pasted image 20240916210643.png | 500]] (the backside of the human eye)

The retina is the tissue that is located at the back of the eye. It receives the light, via it's photoreceptors, either 'rods' or 'cones', which then convert the light to electrical signals, which are then processed by the bipolar cells. The bipolar cells serve as the intermediary between the photoreceptors and the ganglion cells. 

The bipolar cells then transmit the the electrical signals to the dendrites of the ganglion cells, and after the neuron receives them, the ganglion cell then delivers those signals down to the visual cortex via its axons.

prior to getting to the visual cortex, the electrical signals are sent to thalamus, a type of 'control center' for all senses experienced by a human (except smell). the neurons within it process the data before being sent to the visual cortex.

more specifically, visual information is sent to the lateral geniculate nucleus (LGN) to process the visual information.

the LGN processes information such as the contrast and brightness, distinguishes colors, and spatial and temporal frequencies of the electrical signals.

the LGN sends the processed electrical signals once more through sets of axon, which are contained in fibers called optic radiations. they directly connect the LGN to the visual cortex.


through the optic radiations, the lgn passes the electrical signals hierarchically, as:

$LGN \rightarrow V1 \rightarrow V2 \rightarrow V4$

Each portion of the brain (or analogously, *layer*) extracting more complexity from the electrical signals.

the receptive visual fields of neurons tend to increase in size as we progress through each of the visual areas oin the visual cortex, indicating that as we get through ech layer of the visual cortex, each region is able to detect more complex information.

- In **V1 (Primary Visual Cortex)**, neurons primarily respond to simple features such as **edges and orientations**.
- Moving to **V2 (Secondary Visual Cortex)**, the receptive fields become larger, allowing for the detection of more complex patterns and textures.
- In **V3**, the receptive fields continue to grow, enabling the processing of motion and more intricate forms.
- By **V4**, neurons respond to **complex colors and shapes**, integrating information across broader areas of the visual field.
- Finally, in **V5 (Middle Temporal Area)**, the receptive fields are at their largest, specialized for detecting **motion** across extensive visual scenes.

The processing as we go forward becomes more abstracted and integrated, we have more in context understanding as we head towards the $V5$.

The visual cortex also performs 'pooling', as as the simple cells and their multiple smaller receptive fields transfer information to the more complex cells and their larger receptive fields, the complex cells aggregate the activity from the simple cells through pooling. Essentially, the pooling allows for complex cells to have spatial invariance in their repsonse. Despite simple cells activating at different locations, the complex cells activated in similar regions due to the pooling mechanism


**Huber and Wiesel Experiment**

The idea was to record electrical signals from a cat's brain, as the cat was shown moving shapes on a projection screen. 

From this the peeps were able to derive how the visual cortex of a cat works

**CNNs**

1980,  Neocognitron was built by Kinihiko Fukushima, designed based on the current knoweldge about the biologicla visual system. Of course, LeCunn et al formulated this into the development of CNNs, to learn via backpropagation.


---

