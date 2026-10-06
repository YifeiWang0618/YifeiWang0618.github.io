---
title: "Lecture 1: Introduction"
description: Brief notes on the roots of computer vision and deep learning.
view_count_path: /blog/cs231n/lec1/
---

## Beginning

CS231n sits at the intersection of computer vision (CV) and deep learning (DL). The first lecture traces how ideas from neuroscience, early vision research, and neural networks came together. These are my brief takeaways from that overview.

{% include figure.liquid path="/assets/img/cs231n/lec1-fields.png" alt="Diagram placing CS231n at the intersection of computer vision and deep learning, alongside several related disciplines" caption="Where CS231n fits." avoid_scaling=true zoomable=true %}

## From images to understanding [CV]

Biological vision has long inspired computer vision. A camera or retina receives a 2D image of a 3D world; the challenge is to infer useful information about objects, depth, and scene structure. Having two eyes provides one cue to depth, but visual understanding involves much more than binocular vision.

Image classification, assigning a category to an image, is a foundational CV task. It also supports more complex work, such as object detection and scene understanding.

{% include figure.liquid path="/assets/img/cs231n/lec1-marr.png" alt="David Marr's stages of visual representation, from an input image through sketches to a three-dimensional model" caption="Marr's proposed stages of visual representation (Marr, 1982)." avoid_scaling=true zoomable=true %}

## Lessons from visual neurons [CV]

Two observations about the visual system are especially useful here (Hubel and Wiesel, 1959, 1962):

{% include figure.liquid path="/assets/img/cs231n/lec1-receptive-fields.png" alt="Hubel and Wiesel's experiments illustrating responses of simple and complex cells to visual stimuli" caption="Simple and complex cells in the visual cortex." avoid_scaling=true zoomable=true %}

1. **Processing for Local receptive fields.** **Simple cells (inspiration for convolution)** detect oriented features at specific positions within local receptive fields. **Complex cells (inspiration for pooling)** pool responses from similarly tuned simple cells across nearby positions, making them less sensitive to small shifts in a feature’s location. A visual neuron responds to stimuli in a limited part of the visual field instead of processing the whole image at once.
2. **Hierarchical processing (inspiration for stacked layers).** Signals feed into later stages, where simpler features can be combined into more complex representations.

## From early vision systems to deep learning [DL]

The later growth of deep learning depended on progress in three areas: **computing power, data, and algorithms**, which together enabled the advent of the AI era.

- **Face detection:** Viola and Jones's 2001 detector was one of the early successful applications of machine learning to vision. Face detection later became a familiar feature in digital photography (Sony, 2009).
- **Biologically inspired networks:** Fukushima's 1980 _Neocognitron_ drew on the simple and complex cell hierarchy. Its alternating stages anticipated the convolution and pooling operations used in later convolutional networks, though it was not trained like modern deep networks.

The thread connecting these ideas is a move from local visual signals toward increasingly useful representations of the world.

## References

1. Fei-Fei Li, Ehsan Adeli, and Zane Durante. [_CS231n Lecture 1: Introduction, Part 1_](https://cs231n.stanford.edu/slides/2025/lecture_1_part_1.pdf). Stanford University, April 1, 2025. Slides 12, 19, and 22 are reproduced above.
2. David Marr. [_Vision: A Computational Investigation into the Human Representation and Processing of Visual Information_](https://mitpress.mit.edu/9780262514620/vision/). W. H. Freeman, 1982. Linked edition: MIT Press, 2010.
3. D. H. Hubel and T. N. Wiesel. “[Receptive fields of single neurones in the cat's striate cortex](https://doi.org/10.1113/jphysiol.1959.sp006308).” _The Journal of Physiology_ 148, no. 3 (1959): 574–591.
4. D. H. Hubel and T. N. Wiesel. “[Receptive fields, binocular interaction and functional architecture in the cat's visual cortex](https://doi.org/10.1113/jphysiol.1962.sp006837).” _The Journal of Physiology_ 160, no. 1 (1962): 106–154.
5. Paul A. Viola and Michael J. Jones. “[Rapid Object Detection Using a Boosted Cascade of Simple Features](https://doi.org/10.1109/CVPR.2001.990517).” _Proceedings of CVPR 2001_, vol. 1, pp. I-511–I-518.
6. Sony Corporation. “[Sony to Showcase Latest DI Products at PMA 2009 Exhibition](https://www.sony.com/en/SonyInfo/News/Press/200903/09-031E/).” Press release, March 3, 2009.
7. Kunihiko Fukushima. “[Neocognitron: A Self-organizing Neural Network Model for a Mechanism of Pattern Recognition Unaffected by Shift in Position](https://doi.org/10.1007/BF00344251).” _Biological Cybernetics_ 36 (1980): 193–202.
