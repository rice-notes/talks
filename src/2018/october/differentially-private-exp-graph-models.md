# The Promise of Differentially Private Social Network Analysis

## networks and relational data
 
* graphs capture relational data between nodes / entries
    * social networks
    * sexual networks
    * twitter
    * financial transactions etc...
* relationships are complex and carry a lot of info, hard to analyze
* data is highly sensitive

Goal: share network data + protect privacy

## privacy as a statistical problem

* individuals share data with a data curator
* governments, businesses, malicious actors, etc... want to make queries on
  this data

why do this?  
* encourage reprod. and replicability
* combine data sources, etc...

standard methods:  

* anonymization / aggregation
    * easy to break, can discover value of 
      $x_i$ from $\bar{X}$ and $\bar{X \setminus x_i}$

## differential privacy

* very specific amount of noise added to the response of queries by the curator
* provable limits on the level of dataset reconstruction given query response 
  error

#### can we cheat the system my asking a question several times?

systems usually implemented to cache a question, i.e. not respond with a new
dp-modified result

## edge dp

* many types of information in a graph / network - what do we want to protect? 
* this talk considers edge privacy (protecting identity of edges between known nodes)
    * consider financial transactions between companies

* idea: graphs are similar if they differ by one edge
* dp: probability distributions should be similar if graphs are similar

#### what does similar mean?:

Given a random variable $Y$ and a graph $x$, modifications of $x$ are
$\epsilon$-private if for all modik;w


$$
P(Y | x)

