# Differentiation

The crucial thing I took away from colah's blog on computational graphs would be this: Forward-mode differentiation tracks how one input affects every node. Reverse-mode differentiation tracks how every node affects one output. That is, forward-mode differentiation applies the operator &part;/&part;X to every node, while reverse-mode differentiation applies the operator &part;Z/&part; to every node.

Forward-mode differentiation would require us to go through the graph a million times to get the derivatives. Reverse-mode differentiation can get them all in one fell swoop! A speed up of a factor of a million is pretty nice!

This is because in the context of training neural networks, we only care about one single output (the loss), and how all the inputs (millions of parameters) matter from this single output. Reverse-mode differentiation gives us exactly that -- the derivative of one output with respect to all inputs in a single backward pass. This is literally backpropagation.

Whether backpropagation and reverse-mode differentiation are exactly the same thing is a matter of framing. Reverse-mode differentiation is the general mathematical technique. Backpropagation is the specific application of that technique to neural networks, with all the practical details of how you store intermediate values (activations) during the forward pass so you can use them during the backward pass. The core algorithm is the same.

"Training neural networks with derivatives? Surely you'd just get stuck in local minima. And obviously it would be expensive to compute all those derivatives." -- This was the trillion dollar question whose answer was "let's give it a shot". And it worked. The local minima concern turned out to be largely overblown in high-dimensional spaces, and reverse-mode differentiation made the computation tractable. Sometimes the best research strategy is just trying the thing everyone assumes won't work.

# References

https://colah.github.io/posts/2015-08-Backprop/
http://neuralnetworksanddeeplearning.com/chap2.html
