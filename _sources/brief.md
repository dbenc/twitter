# Brief

This project tries to find an efficienct routing algorithm on a real world network. For this algorithm to be sucessful, a couple questions are needed to be answeared:
- "What makes the routing possible?"
- "What kind of algorithm should be used?"
- "How the layout of the network determines the sucess of the routing?"
- "How the lenght of the route determines the sucess if the routing?"
- "Is there a difference in routing for different cities?".

## Six degrees

In the famous experiments of Milgarm {cite}`milgram` randoml chosen american citizens
were asked to to deliver a letter to a given address in Boston but they were only
allowed to forward it directly to personal acquaintances. The lenghts of the sucessful 
letter deliveries were between 5 and 6 steps, hence the "six degrees of separation".


## Navigability

The sucess of the routings in the experiments was because the participants did not send
the letters blindly, each of them had an internalized “labeling space” with a distance metric,
meaning if the letter was addressed to Boston, they sent it to someone they know who works
in Boston. So we __hidden metric space__ for the algorithm to be able to use a labeling
space of its own.

In his paper {cite}`Kleinberg2000NavigationIA` Kleinberg presented the idea of a decentralized
__greedy routing__ algorithm, which means at every step makes the locally optimal choice at each
stage of the routing. This type of algorithm is efficient is __the link lengths of the network__ are
distributed according to the power-law $P(d) \sim 1/d$.

Boguna et al. {cite}`Bogu__2008` showed on simulated data that the succes also depend heavily on
the __degree distribution__ $P(k)=k^{-\gamma}$ and the __clustering coefficient__ of the network.
These conditions have been previously examined in other articles {cite}`elte` as well as on social networks.


## Citations

```{bibliography}
```