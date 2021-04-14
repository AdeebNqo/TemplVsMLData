# TemplVsMLData

## Introduction

Does a data-driven approach, rather than a template-based approach, produce more natural text? 

The two systems, one for the template-based approach and one data-drinven one (seq2seq), are described in detail the <a href="https://projects.cs.uct.ac.za/honsproj/cgi-bin/view/2019/dunn_poulter.zip/">E2E page</a> 

## Examples

For illustrative purpose in this readme file, what the systems do, is take a graph as input (based in Wikipedia's people information) and try to generate a human-readable sentence from that. 

graph:
{"Name_ID": "Ted Kleinhans", 
"date of death":  [{"mainsnak": "July 24 1985"}], 
"date of birth": [{"mainsnak": "April 8 1899"}], 
"instance of": [{"mainsnak": "Human"}], 
"sex or gender": [{"mainsnak": "male"}], 
"member of sports team": [{"mainsnak": "Philadelphia Phillies"}, 
{"mainsnak": "Cincinnati Reds"}, 
{"mainsnak": "New York Yankees"}], 
"place of birth": [{"mainsnak": "Deer Park, Wisconsin"}], 
"place of death": [{"mainsnak": "Redington Beach, Florida"}] 

ML-generated sentence: 
Ted Kleinhans (April 8 1899 in Deer Park, Wisconsin -- July 24 1985 in Redington Beach, Florida) was a Major League Baseball pitcher who played for the Philadelphia Phillies Cincinnati Reds and New York Yankees. 

Template-generated sentence:
Ted Kleinhans (April 8 1899 -- July 24 1985) was born in Deer Park, Wisconsin. He played for the Philadelphia Phillies, Cincinnati Reds and New York Yankees. He died in Redington Beach, Florida.

## The data

* Prelimresults.zip contains the details of the first evaluation, with 10 paired sentences that were evaluated by 91 respondents at UCT.
* all_texts.csv contains all the texts (70 paired sentences) that were evaluated on MTurk.
* judgements-without-failed-check.zip is the data obtained from that crowdsourced evaluation, excluding those who failed the attention check.
* The Knowledge graph we used is <a href="https://doi.org/10.18653/v1/w18-6502">described here</a> and accessible at the <a href="https://github.com/EagleW/Describing_a_Knowledge_Base">Dewscribing a Knowledge Base github reposotiry</a>. 

## Contributors

* Zola Mahlaza
* Jarryd Dunn
* Matthew Poulter
* Maria Keet

## Funding
In theory, yes, since it was specified as part of the "Quest: Querying Smart Text" project that was approved for funding in 2019 by SADiLaR, but they still haven't paid. The insights gained are also relevant within the scope of the NRF-funded <a href="http://www.meteck.org/MoReNL/">MoreNL project</a> for surface realisers for African languages.
