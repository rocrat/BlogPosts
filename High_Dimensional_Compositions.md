---
author: Dominic LaRoche
date: YYYY-MM-DD
slug: INSERT\_SLUG\_HERE
status: draft
title: When is a composition not a composition?
categories:
  - r
---
tl/dr; Never.

*What* is a Composition?
========================

Lets first start with the definition of a composition, since many readers may not be familiar with that term. A composition is a set of measurements that sum to an arbitrary whole. These measurements are therefore proportions of the whole and are, by definition, not independent.

A classic example of a composition comes from the study of rocks (otherwise known as geology). Rocks are usually classified by what they are made of, e.g. granite is a mixture of quartz and feldspar. The exact mixture, or proportions, of these ingredients provides further classification. Clearly, the total amount of quartz and feldspar will depend on the size of the rock in question. Two identical specimens of different sizes will be expected to have the exact same proportions, but the total wieght of each part will be directly proportional to the size of the rock.

This all seems very obvious when considering the composition of a rock. But compositions arise in many other scientific pursuits and the compositional properties of the measurements are frequently ignored. For example, in metabolomics a sample is collected and the quantities of certain metabolites are measured, usually as proportions. Or in economics one might study the spending habits of consumers, but the total amount spent might not be as informative as the proportion of an individual consumer's total income. Additionally, many of the technologies at the forefront of the push for 'personalized medicine' result in compositional data. Most notably RNASeq, which measures the expression patterns of an individuals genes, generates relative abundances of gene transcripts with the total number of each transcript depending on several techincal or experimental factors which are of no interest biologically.

Why should I care about compositions?
=====================================
