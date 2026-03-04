# Rediscovering JEPA: Part I

I have no idea what JEPA is, all I know is that the full form of JEPA is joint embedding predictive analysis, or something along those lines. I also do not have much strong idea of free energy principle that was recently discovered about brains. Finally, I also have very little idea about how Energy Based Models (EBM) work. I try to think of these topics from first principles, see if I am able to derive some or the other directlty from my own thoughts, while having a chat with Claude. In general, I end up discussing my ideas with Claude, and it spoils me with information of how they might be related to what is already out there, it's also the reason why I was able to list out the above topics as I did, without knowing about them apriori.

I start this discussion with the simple thought that when I read the title of the book, my brain makes a prediction about the contents of the book. As more information is fed to me, the most natural state change is the one that requires the least amount of effort from my side, as well as fits with the new data. If the new data is too much, then it may either overwrite my entire prediction or it may lead my brain into a contradictory state of affairs. An event that is more surprising to the brain, is the one that does not match the prediction already made. Such events are also more expensive for the brain to accomodate, since my own prediction, my own world model changes significantly. The under the carpet definition of "surprise" here could mean "Shannon surprise" or "Bayesian surprise" and one of them makes more sense to me than the other. A person truly expecting surprise, that may very well have Shannon surprise calculated by -log p(observation) while this may be expected for the person. The calculation of surprise, and hence the effort required to readjust the model implicitly assumes some world model of the person, and hence the calculations too must have the prediction distribution in the picture if it were to give an accurate measure.

This is relative entropy, or KL divergence. The formula is: 

$$
S(D, M) = KL(P(M | D), P(M)) = \sum_M P(M|D) \log \frac{P(M|D)}{P(M)}
$$

Here $P(M)$ is the prior distiribution of the observer about the background, or the world. $D$ is the new data or the observation that took place. If $D$ presents no surprise, then it does not impact the distribution whatsoever. $P(M|D) = \frac{P(D|M)}{P(D)} P(M)$ comes from Bayes' theorem (for reference). The formula for KL divergence measures the extra amount of surprise the distribution $P(M|D)$ gives in comparison to the surprise you would get if you believed the distribution is $P(M)$. To put in context, cross entropy $H(P, Q)$ measures the amount of surprise if you observe the distribution $P(M)$ but you expected that the distribution should have been $P(Q)$. From this you just subtract if you believe it to be $P(M)$ as well. Minimizing KL divergence is minimizing the relative amount of surprise that you observe from the real world if your understanding was based on the model, the information theoretic POV also says that KL divergence is the average amount of bits wasted if your code was built for $Q$ but the actual code turned out to be $P$.

> Across all these fields, KL divergence measures the same thing: the cost of using the wrong model of reality.

Effort to adjust the prior distribution to the new distribution is path dependent, simpler explainations require lesser effort. Now a simpler explaination would be the one that does not have any high entropy claims on the way. There are a lot of supporting theories that I can use here, but I'll try to stick to cognitive science and infromation theory.

> What makes an activity effortful? A simple (and perhaps simplistic) answer is that effortful activities involve maintaining something in a state that it is not normally in. For instance, if you were to raise your arm and keep it in the air it will become progressively effortful to maintain this posture. However, it takes very little effort to keep your arm by your side—a posture that is much more common

Effort being path dependent flows well with our understanding of the way we humans learn. The same knowledge or information can be learned in very different ways, one could be very effortful while the other comes _naturally_ to us. The formula stated in Karl Friston's paper re-uses KL divergence. This time, the KL divergence is between the habitual state of mind, and the state of mind that falls in the path of understanding. The high entropy might make sense to you now, it is in reference to your habitural state leading us to KL divergence. The repeated force of the state of mind heading away from the habitual state, in direction of a particular state leads to the habitual state itself shifting towards the latter. Apparently this is called active inference.




# References

http://ilab.usc.edu/surprise/
https://pmc.ncbi.nlm.nih.gov/articles/PMC10636588/
