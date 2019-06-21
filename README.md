# Gradient-Checking
In this project, I have performed 'Gradient Checking' to check whether the backpropogation is working fine. Popular deep learning libraries such as Tensorflow, Keras have a well coded forward propogation and backwar propagation included with them. But when we build our own neural networks, we cant be sure that our neural network works fine all the time. In such cases, we could make use of gradient checking to ensure we are on the right track!


1) What is gradient checking and How does gradient checking work?



Backpropagation computes the gradients  ∂𝐽∂𝜃 , where  𝜃  denotes the parameters of the model.  𝐽  is computed using forward propagation and your loss function.

Because forward propagation is relatively easy to implement, you're confident you got that right, and so you're almost 100% sure that you're computing the cost  𝐽  correctly. Thus, you can use your code for computing  𝐽  to verify the code for computing  ∂𝐽∂𝜃 .

Let's look back at the definition of a derivative (or gradient):
∂𝐽∂𝜃=lim𝜀→0𝐽(𝜃+𝜀)−𝐽(𝜃−𝜀)2𝜀(1)

If you're not familiar with the " lim𝜀→0 " notation, it's just a way of saying "when  𝜀  is really really small."




We know the following:

∂𝐽∂𝜃  is what you want to make sure you're computing correctly.

You can compute  𝐽(𝜃+𝜀)  and  𝐽(𝜃−𝜀)  (in the case that  𝜃  is a real number), since you're confident your implementation for  𝐽  is correct.
Lets use equation (1) and a small value for  𝜀  to convince your CEO that your code for computing  ∂𝐽∂𝜃  is correct!
