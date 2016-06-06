Apartment Rental Benchmarking (ARB)
MCMC simulations of apartment rent finance and outcomes
Linux / R programming language exercise
(C) Jukka Paulin 
2012

This memo drafts both a real-world simulator for apartment
renting and a computer game derived from the idea(s). 

The ARB is a simulation of rent-letting, in the environment
of a Market (of houses). The activity takes place in
iterations, or rounds. With each individual round only 
a handful of different actions can happen. The simulation
can accomodate to two main modes: without a "letting agent"
(the landlord acts solo), or using an agent as a facilitator
between the landlord and the tenant.  

A discrete MCMC simulation model is used. This means essentially
that 
 (a) the simulation advances in steps (='it is discrete')
 (b) Monte Carlo 

The simulation is centered around a single house for
rental (the Apartment). The house can be occupied or free;
if it is occupied, the owner gets a sum of money each
month (assuming the tenant is honest).

The simulation branches as time advances, and there are interesting
end-points where the agents of this simulation have
experienced different "train" of events. Randomness (luck)
has a saying in the outcome of the simulation, as does
other factors.  

The simplified version of this program just loops through
N iterations and spills out the results. This version
contains (7) of the basic nine events. The neglected
events are those two that have to do with using couriers
as middlemen in the renting business. 

The real beef of the simulation is scenario analysis. 
Scenarios can be made by tweaking static variables or
touching the limits of random variables.  

Function definitions

The ARB simulates how rental activity (owning a house and
renting it directly or indirectly via couriers) takes 
different kinds of paths according to events. 

Nine Eventcodes
---------------

The events can be one of the (9) possible:
 - seeking a new candidate to occupy the rental house
 - forming or purging an rental agreement
 - the candidate purges a rental agreement
 - the rental agreement is expired and not continued
 - the rental agreement expires and is continued 
 - forming or purging a courier agreement
 - selling the property
Advanced events include (2) more:
 - candidate neglects the agreement by not paying rent
 - candidate neglects the agreement and causes damage to apartment

===================================
Program skeleton
===================================
<WIP>

Data structures
===============
- data structures are quite simple
- things to keep record of are
  - each house status: 
    - tenant currently, or None 
    - if None, then a code that signifies one of Nine Eventcodes  

Markets
- demand
- reasons for demand

Population density and other interesting statistics
- square kilometers used as areal unit

How does the simulation work?
=============================

We keep notice of the vacancy of the apartment. This is 
stored in the variable Y. 
Y can have only two states: 0 = empty, 1 = vacant

Qualitative research vs. quantitative
=====================================

- qualitative is about the "human" side of an issue; often
  contradictory behaviors, beliefs, opinions, emotions and
  relationships of individuals
- qualitative research is also effective in identifying
  intangible factors, such as social norms, socioeconomic
  status, ...


