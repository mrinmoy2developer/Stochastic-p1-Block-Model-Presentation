# Stochastic-p1-Block-Model-Presentation
A class presentation in my undergraduate years for Stat Comprehensive.
## Overview
* In 1959 Paul Erdos and Alfred Renyi also Gilbert defined a very simple single parameter structure to model random graphs.
* In 1972 Jaroff and Ratcliff gave a generalised iterative algorithm called 'Iterative scalling Algo' for approximating maximum likelihood estimators of a wide class of distributions where the probabilities are in 'product form'.Holland et. al used this method to fit the p1 model.Later on Wang and Wong also used a modified version of this algo for fitting their blocked version.
* Generalizing Erdos-Renyi's model, in 1981 Holland Leinhardt proposed their p1 model with 4 parameters with 2 of them vectors for modeling social networks. It was still quite mathematically sound with nice properties and asyptotic distributions.
* Again in 1987 Holland's phd scholar Yuchung Jeff Wang from Carnegie Melon University modified the probability of assymetic dyads theta_ij to a non-additive one by adding a block parameter to it.

In this presentation these 4 papers are discussed and 2 emperical examples are explored:-
* The Sampson's Monastry Experiment(1969)
* The Hansell's Elementary school Experiment(1984) 

## Summary of the Problem and Approaches:-
Modelling directed random graphs especially for social networks using various exponential family distributions.
* The original [Erdos-Renyi model](https://github.com/mrinmoy2developer/Stochastic-p1-Block-Model-Presentation/blob/4f6d5722dc77b2cf154fde574bd47a370c3d3e52/Research%20Papers/eardos%20renyi%20gilbert.pdf) had a single parameter p and the edges were essentially iid bernoulli(p). It's simple with nice asyptotic properties but is based on  rather unrealistic assumptions for most practical applications.  
* Next the [Holland & Leinhardt's vanilla p1 model](https://github.com/mrinmoy2developer/Stochastic-p1-Block-Model-Presentation/blob/4f6d5722dc77b2cf154fde574bd47a370c3d3e52/Research%20Papers/Holland%20-%201981%20-%20An%20Exponential%20Family%20of%20Probability%20Distributions%20for%20Directed%20Graphs.pdf) was based on 4 parameters: theta, alpha_i, beta_j, & rho_ij where i,j runs from 1 to n. Here theta is interpreted as the base edge density factor, alpha_i's are the expansiveness factor while beta_j's are the attractiveness factor, and rho_ij's are the reciprocation parameter. This model was unable to model the local subgroups that are generally present in a community.
* Lastly the [Wang & Wong's p1-block model](https://github.com/mrinmoy2developer/Stochastic-p1-Block-Model-Presentation/blob/4f6d5722dc77b2cf154fde574bd47a370c3d3e52/Research%20Papers/Wang%20-%201987%20-%20Stochastic%20blockmodels%20for%20directed%20graphs.pdf) solved this issue by introducing block parameters lambda_kl. MLE's for both the p1 and p1-block model exists and can be expressed inplicitly by equating the sufficiency statistics in each case to their expectation.But in practice, an iterative approach, called [Darroch & Ratcliff's <b>Iterative Scalling Algorithm</b>](https://github.com/mrinmoy2developer/Stochastic-p1-Block-Model-Presentation/blob/4f6d5722dc77b2cf154fde574bd47a370c3d3e52/Research%20Papers/iterative%20Scalling%20Algorithm.pdf) is used to approximate these estimates.

## Emperical Examples:-
<figure>
<img src="https://user-images.githubusercontent.com/35917115/229427211-7855b120-599a-4f8d-884d-d7c18013cce3.png" alt="Trulli" style="width:100%">
<figcaption align = "center"> <b>The Sampson's Monastry Experiment(1969):- The data stem from an ethnographic study of community structure in a New England monastery by Samuel F. Sampson,1969. The study describes several social relations among a group of men (novices) who were preparing to join a monastic order. The data sets presented here contain the affect relations among the novices, which were collected by asking them to indicate whom they liked most and whom they liked least. The novices were asked for a first, second, and third choice on both questions. The social relations were measured at five moments in time. The fourth measurement (at time T4) took place one week before four of the novitiates were expelled from the monastery.
Some novices had attended the minor seminary of 'Cloisterville' before they came to the monastery.Based on his observations and analyses, Sampson divided the novices into four groups: Young Turks, Loyal Opposition, Outcasts, and an interstitial group. The Loyal Opposition consists of the novices who entered the monastery first. The Young Turks arrived later, in a period of change. They questioned practices in the monastery, which the members of the Loyal Opposition defended. Some novices did not take sides in this debate, so they are labeled 'interstitial'. The Outcasts are novices who were not accepted in the group.

</b></figcaption>
</figure>

<figure>
<img src="https://user-images.githubusercontent.com/35917115/229427323-d99c70f4-6b03-458f-883d-fe0284918ad3.png" alt="Trulli" style="width:100%">
<figcaption align = "center"><b>The Hansell's Elementary school Experiment(1984):- This study was conducted by Hansell (1964) at Rutgers University, New Brunswick. It involved 317 fifth and sixth-grade students in an inner-city Baltimore elementary Our consists of 13 male and l4 female sixth graders from a single classroom. The students were were asked to indicate their liking for each student by choosing one of the three facial expressions: (a) a big smile and labeled "a lot," (b) a moderate smile and labeled "some," and (c) no smile and labeled "not much." Choice (a) suggests a strong friendship tie and is coded as 1 in the socio-matrix , whereas choices (b) and (c) indicate weak ties and are coded as 0. 
 </b></figcaption>
</figure>

