---
title: A Brief Review of Hyperparameter Optimization Methods for Machine Learning
theme: white
revealOptions:
  transition: 'slide'
  controls: true
  slideNumber: true
---

# A Brief Review of Hyperparameter Optimization Methods for Machine Learning

<small>Richard Wen</small>  
<small>rwen@ryerson.ca</small>  
<small>Department of Civil Engineering</small>  
  
<small>November 29, 2017</small>  
  
<small>*Presentation for Research Methods in Computer Science Course Instructed by Dr. Cherie Ding.*</small>

---

# Outline

1. Introduction
2. Methods
3. Results
4. Discussion
5. Conclusion
6. References

---

# Introduction

---

## Machine Learning

* Learn from data
* Accuracies > 99% possible
* Real-world applications

---

### Object Detection and Tracking

<!-- .slide: data-background="./edit/img/raccoon_objdetect.gif" -->

---
 
### Medical Image Diagnoses

<!-- .slide: data-background="./edit/img/ctscan_thorax.gif" -->

---

### Disaster Mapping

<!-- .slide: data-background-iframe="./edit/iframe/simontontexas_harveyflood/simontontexas_harveyflood.html" -->

---

## Machine Learning Process

<img src="./edit/img/mlprocess.svg"></img>

---

## Machine Learning Model

<img src="./edit/img/mlmodel.svg"></img>

---

## Hyperparameters

* Adjustable values
* Affect learning performance
* Before learning process

---

## Hyperparameter Optimization

* Adjustable values $x \dots x_n$
* Affect performance measure $f$
* Find optimal $x \dots x_n$

$$
\underset{x \dots x_n}{\operatorname{argmax}} f(x \dots x_n)
$$

---

## Objectives

For hyperparameter optimization:

1. `Summarize` recent methods
2. `Discuss` limitations
3. `Propose` improvements and future directions

---

# Methods

---

## Methods Process

<img src="./edit/img/methodsprocess.svg" margin="500px"></img>

---

## Digital Library Selection

<img src="./edit/img/cs_jif_graph.png" width="65%"></img>

<small>Top 25 computer science journals on InCites by Journal Impact Factors</small>

---

## Automatic Search Queries

Query| Value
--- | ---
`Publication` | IEEE or ACM
`Year`| 2014 to October 5, 2017
`Title contains` | *hyperparameter*, *optimization*

---

## Manual Selection Criteria

Criteria| Description
--- | ---
`Detailed` | specific methods and results, >= 8 pages
`Relevant`| mention hyperparameter optimization
`Practical` | experiments, benchmarks, applications

---

## Review Procedure

1. `Identify` methods
2. `Summarize` methods
3. `Summarize` experiments and results
4. `Discuss` limitations, improvements, directions

---

# Results

---

## Potential Papers

<canvas class="chart">
<!--
{
 "type": "bar",
 "data": {
  "labels": ["2014"," 2015"," 2016"," 2017"],
  "datasets":[
   {
    "data":["0", "0", "0", "2", "0", "8"],
    "label":"ACM","backgroundColor":"rgba(91, 194, 244, 0.8)"
   },
   {
    "data":["1", "3", "4","4"],
    "label":"IEEE Xplore","backgroundColor":"rgba(0, 45, 114, 0.8)"
   }
  ]
 }, 
 "options": { "responsive": "true" }
}
-->
</canvas>

---

## Selected Papers

<canvas class="chart">
<!--
{
 "type": "bar",
 "data": {
  "labels": ["2014"," 2015"," 2016"," 2017"],
  "datasets":[
   {
    "data":["1", "3", "4", "6", "0", "8"],
    "label":"Potential","backgroundColor":"rgba(91, 194, 244, 0.8)"
   },
   {
    "data":[" 0", "2", "1", "2"],
    "label":"Selected","backgroundColor":"rgba(0, 45, 114, 0.8)"
   }
  ]
 }, 
 "options": { "responsive": "true" }
}
-->
</canvas>

<span class="reference">Ref: [1-5] (Selected Papers)</span>

---

## Hyperparameter Optimization Methods

1. `Simple`: Exhaustive search
2. `Advanced`: Model or procedural based search

---

## Simple Methods

Method | Description
--- | ---
`Manual Search` | Trial and error
`Grid Search` | Predefined range of values
`Random Search` | Randomized range of values

<span class="reference">Ref: [6] </span>

---

## Manual Search

Hyperparameter | Values
--- | ---
$x_1$ | 5
$x_2$ | 10
$x_3$ | 15

---

## Grid Search

Hyperparameter | Values
--- | ---
$x_1$ | 5, 10, 15
$x_2$ | 3, 6, 9
$x_3$ | 2, 4, 6

---

## Random Search

Hyperparameter | Values
--- | ---
$x_1$ | <span class="random"></span>, <span class="random"></span>, <span class="random"></span>, <span class="random"></span>
$x_2$ | <span class="random"></span>, <span class="random"></span>, <span class="random"></span>
$x_3$ | <span class="random"></span>, <span class="random"></span>

---

## Advanced Methods

Method | Description
--- | ---
`Assumption` | Expert assumptions for particular cases
`Evolutionary` | Procedurally generated hyperparameters
`Sequential Model` | Sequentially guided hyperparameters

---

## Assumption Based Optimization

* Specific algorithms, data, and cases
* Select $x \dots x_n$ based on assumptions
* e.g. Distribution assumptions

<span class="reference">Ref: [1] </span>

---

## Evolutionary Based Optimization

* Mimic biological evolution
* Evolve and naturally select $x \dots x_n$
* e.g. Genetic algorithms, particle swarm

<span class="reference">Ref: [7]</span>

---

## Sequential Model Based Optimization (SMBO)

* Model performance function $f$ using $x \dots x_n$
* Predict next best set of hyperparameters
* e.g. Bayesian optimization, random forest

<span class="reference">Ref: [8-10] </span>

---

## SMBO Improvements

* Transfer learned hyperparameters [1]
* Discover better starting hyperparameters [2]
* Measure transfer hyperparameters influence [3]
* Consider hyperparameter inter-dependency [4]

---

## SMBO Experiments

* Improved performance (e.g. ~10-20%)
* Better hyperparameters than simple methods
* Same time and iteration constraints

---

## SMBO Data

<canvas class="chart">
<!--
{
 "type": "bar",
 "data": {
  "labels": ["Real-world", "Repository", "Library"],
  "datasets":[
   {
    "data":["2", "2", "3", "0", "8"],
    "label":"# of datasets","backgroundColor":"rgba(0, 45, 114, 0.8)"
   }
  ]
 }, 
 "options": { "responsive": "true", "scaleSteps" : "1"}
}
-->
</canvas>

<span class="reference">e.g. WEKA, 1000 Genomes; 50+ datasets; ~500-60000 instances</span>

---

# Discussion

---

## Limitations

* Manual constraints selection
* Scalability
* Dataset variability

---

## Manual Constraints

* Hyperparameters $x \dots x_n$
* Performance measure $f$
* Set of constraints $C$
* Iteration or steps $t$

$$
\underset{x \dots x_n \in C}{\operatorname{argmax}} f(x \dots x_n) \textrm{ given } t
$$

---

## Improvements and Future Directions

* Automated Machine Learning
* Combining methods
* Sampling

---

# Conclusion

* Reviewed 5 papers
* SMBO as an effective framework
* Constraints and scalability
* Automated Machine Learning

---

# References

---

* [1] N. Schilling, M. Wistuba, L. Drumond, and L. Schmidt-Thieme, “Joint
model choice and hyperparameter optimization with factorized multilayer
perceptrons,” in 2015 IEEE 27th International Conference on Tools
with Artificial Intelligence (ICTAI), Nov 2015, pp. 72–79.
* [2] M. Wistuba, N. Schilling, and L. Schmidt-Thieme, “Learning hyperparameter
optimization initializations,” in 2015 IEEE International
Conference on Data Science and Advanced Analytics (DSAA), Oct 2015,
pp. 1–10.

---

* [3] M. Wistuba, N. Schilling, and L. Schmidt-Thieme, “Hyperparameter optimization machines,” in 2016 IEEE International
Conference on Data Science and Advanced Analytics (DSAA),
Oct 2016, pp. 41–50.
* [4] J. C. L`evesque, A. Durand, C. Gagn`e, and R. Sabourin, “Bayesian optimization
for conditional hyperparameter spaces,” in 2017 International
Joint Conference on Neural Networks (IJCNN), May 2017, pp. 286–293.

---

* [5] A. Quitadamo, J. Johnson, and X. Shi, “Bayesian hyperparameter
optimization for machine learning based eqtl analysis,” in Proceedings
of the 8th ACM International Conference on Bioinformatics,
Computational Biology,and Health Informatics, ser. ACM-BCB ’17.
New York, NY, USA: ACM, 2017, pp. 98–106. [Online]. Available:
http://doi.acm.org/10.1145/3107411.3107434
* [6] J. Bergstra and Y. Bengio, “Random search for hyper-parameter optimization,”
Journal of Machine Learning Research, vol. 13, no. Feb, pp.
281–305, 2012.

---

* [7] D. Whitley, S. Rana, J. Dzubera, and K. E. Mathias, “Evaluating
evolutionary algorithms,” Artificial intelligence, vol. 85, no. 1, pp. 245–
276, 1996.
* [8] J. Snoek, H. Larochelle, and R. P. Adams, “Practical bayesian optimization
of machine learning algorithms,” in Advances in neural information
processing systems, 2012, pp. 2951–2959.

---

* [9] F. Hutter, H. H. Hoos, and K. Leyton-Brown, “Sequential model-based
optimization for general algorithm configuration.” LION, vol. 5, pp. 507–
523, 2011.
* [10] D. R. Jones, M. Schonlau, and W. J. Welch, “Efficient global optimization
of expensive black-box functions,” Journal of Global optimization,
vol. 13, no. 4, pp. 455–492, 1998.

---

# Thank you

<small>Richard Wen</small>  
<small>rwen@ryerson.ca</small>  
<small>Department of Civil Engineering</small>  
  
<small>[github.com/rrwen/slides-rmcs-litreview](https://github.com/rrwen/slides-rmcs-litreview)</small>  
