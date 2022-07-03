## DEF

  __BLANK__

## GOAL

Ship a solution for real-time hit classification.  


## PAST WORK

- Unsupervised: GC
- Supervised: CNN model, YOLOv2 model.
  - Data Labeling: 100+ images labeled per class.  


## CHALLENGE

- [G] They are very slow to train.
  - My case
    - 7.6 iter/s => 0.131579 s/iter
    - 10 s/epoch => 60 epoch := 600 s := 10 min
  - CNN (Unknown)
  - YOLOv2
    - 100 iter/280s := 2.8 s/iter => 4000 iter := 11200.0 sec := 186 min := 3 hours.
- [G] Absolutely not generalizable even when data variety is rich enough.


## MY PROPOSED APPROACH

- [G] Triplet loss without FC layer, very efficient to train.  
- [G] Embedding learning method is generalizable.  

### How to diagnose our training

- [G] Estimate how good are our training examples.  
  [G] (Variety of hit matters).
  - [G] Recall is a good indicator for real-time labeling.
    [G] imagine all 40 hits look similar, it won't work. Recall of multi-hit will tell it.
- [O] Data augmentation enables training on small number of uniquely labeled images.
  - [O] Saving manual labeling effort.

### Property in real-time solution

- [G] Estimate the speed of how many images can be processed (in Hz).
  - [G] Psana1 performance (raw is 400 Hz, calib is 9 Hz, image is 8 Hz).
- [O] We provide a human baseline.  

### Implications

- [O] The closest solution to real-time classification (human-in-the-loop).  
- [O] It shows potential for a no-human-in-the-loop solution.


## EXPERIMENTS SHOWING VALIDITY

- 80 images performance.
  - Show **variety** is the key and **recall** is the indicator.
  - Show augmentation enhances model training.

- Generalizability performance
  - Show its performance on big particles.  

- Estimate the Hz
  - psana speed
  - CPU to GPU speed
    - Bigger batch might not be good.

<!--
DARPA operates on the principle that generating big rewards requires taking big
risks. But how does the Agency determine what risks are worth taking?

George H. Heilmeier, a former DARPA director (1975-1977), crafted a set of
questions known as the "Heilmeier Catechism" to help Agency officials think
through and evaluate proposed research programs.

- What are you trying to do? Articulate your objectives using absolutely no
  jargon.
- How is it done today, and what are the limits of current practice?
- What is new in your approach and why do you think it will be successful?
- Who cares? If you are successful, what difference will it make?
- What are the risks?
- How much will it cost?
- How long will it take?
- What are the mid-term and final “exams” to check for success?
-->
