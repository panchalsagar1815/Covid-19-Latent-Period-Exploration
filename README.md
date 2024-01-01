# Covid-19-Latent-Period-Exploration

Abstract
The incubation period for the COVID-19 is reported. We can't say the same for the latent period (the period since the person is infected but has not spread the infection yet), which is a vital characteristic of every infectious disease. Knowing the latent period gives an ability to run simulations which are far more accurate. In this study, I try to estimate the latent period for COVID-19 caused by the SARS-CoV-2 virus via computational simulations using SEIR model with different values controlling the latent period length (e.g. latent period parameter sweep). I try to fit all other parameters to match the observed statistics the best. I do such modelling for 5 different locations worldwide which are currently experiencing different stages of the epidemic.

As a result, Europe locations suggest that latent period is between 2 and 4 days: Austria case suggests the value of 48-96 hours, Italy case suggests the value greater than 48 hours. While China cases suggest shorter latent period.

Introduction
The data
I use the time series data (infected count, recovered count and deaths count) published by the John Hopkins University as ground truth observations.

I experiment with these 5 locations:

Austria (infection peak has passed)
Beijing, China (there were 2 peaks)
Heilongjiang, China (two more distinct peaks)
Italy (Peak is approaching)
South Korea (single peak passed long ago)
Latent period estimation
The latent period can be estimated as reciprocal to the sigma parameter. Thus latent period = 1.0 / sigma

The parameter fitting procedure
I let the optimizer to fit the following parameters:

Infection start date
number of the exposed people count on the first day of infection
number of the infected people count on the first day of infection
beta (separate value per week) - infection rate
gamma - recovery rate
