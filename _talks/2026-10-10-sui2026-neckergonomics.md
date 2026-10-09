---
title: "NeckErgonomics: Adapting Head Rotation in HMDs with Predicted Neck Muscle Activity"
collection: talks
type: "Conference talk"
talk_type: "Conference talk"
permalink: /talks/2026-10-10-sui2026-neckergonomics/
venue: "ACM Symposium on Spatial User Interaction (SUI 2026)"
date: 2026-10-10
location: "Bari, Italy"
slidesurl: "/files/NeckErgonomics_SUI26_slides.pdf"
excerpt: "I presented NeckErgonomics at ACM SUI 2026: a model trained on neck EMG predicts neck muscle activity from head tracking, and three VR interaction techniques use it to reduce neck effort."
---

I presented our paper **NeckErgonomics** at **ACM SUI 2026** in Bari, Italy, with a pre-recorded talk.

![Title slide]({{ site.baseurl }}/images/talks/sui2026/slide01-title.jpg)

## Why the neck?

In head-mounted displays, the head is the controller. We point, read and look around 360° content by turning the head, and the headset adds extra load in front of the face. As XR sessions get longer, neck strain becomes a matter of usability and accessibility, not only comfort.

![In HMDs, every head movement is work for the neck]({{ site.baseurl }}/images/talks/sui2026/slide02-problem.jpg)

## A model of neck muscle activity

We trained a small neural network on our open neck EMG dataset. It takes head yaw, pitch and fixation time and predicts neck EMG. No extra sensors are needed at runtime: the headset's head tracking is enough.

![We trained a model on our neck EMG dataset]({{ site.baseurl }}/images/talks/sui2026/slide04-model.jpg)

## One signal, three interaction techniques

The interface helps more when predicted neck effort is high, and behaves normally near the comfortable forward pose.

![NeckErgonomics: adapt to predicted neck effort]({{ site.baseurl }}/images/talks/sui2026/slide06-approach.jpg)

**Head pointing:** the cursor moves further than the head when turning is costly.

![Head pointing with model-based cursor gain]({{ site.baseurl }}/images/publication_figures/NeckErgonomics/1_head_pointing.gif)

**Reading:** a window off to the side glides back to the front, so the head can follow it to a neutral pose.

![Reading with model-based window recentering]({{ site.baseurl }}/images/publication_figures/NeckErgonomics/2_reading.gif)

**360° video:** the view turns further than the head, so you can look behind you without turning all the way.

![360° video with model-based viewport amplification]({{ site.baseurl }}/images/publication_figures/NeckErgonomics/3_360_video.gif)

## Study and results

We ran a within-subjects study with 18 participants on a Meta Quest 3, one task per technique.

![Study design]({{ site.baseurl }}/images/talks/sui2026/slide10-study.jpg)

- **Pointing:** less head movement, but slower and less precise on small targets.
- **Reading:** less head rotation and higher comfort.
- **360° video:** lower physical demand, with no extra sickness.

![Pointing results]({{ site.baseurl }}/images/talks/sui2026/slide11-results-pointing.jpg)

![Reading results]({{ site.baseurl }}/images/talks/sui2026/slide12-results-reading.jpg)

![360° video results]({{ site.baseurl }}/images/talks/sui2026/slide13-results-360.jpg)

## What we learned

![What we learned]({{ site.baseurl }}/images/talks/sui2026/slide14-takeaways.jpg)

[Download the slides (PDF)]({{ site.baseurl }}/files/NeckErgonomics_SUI26_slides.pdf)

[Read the paper]({{ site.baseurl }}/publication/2026-10-10-neckergonomics-adapting-head-rotation)
