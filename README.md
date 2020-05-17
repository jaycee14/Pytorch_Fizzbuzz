# Pytorch_Fizzbuzz
Recreation (overkill!) of Fizzbuzz in Pytorch

## Rationale

I wanted a small self contained project to help my understanding of Pytorch.
Joel Grus's [excellent blog post](https://joelgrus.com/2016/05/23/fizz-buzz-in-tensorflow/) was the source of this idea and is highly worth a read. I've even borrowed some of his functions.

The classic [Fizzbuzz](https://en.wikipedia.org/wiki/Fizz_buzz) problem can be solved imperically in a few lines of code so creating a neural network is a total overkill but its still a very interesting small project when learning the details of a designing a network, deploying to a GPU and a chance to dig into the basics. 

It's also still powerful to show a pattern being learnt with data alone. 

## Update

I demo'd this to my AI study group - more as a pytorch demo - it kicked off a conversation about whether a simple DNN could ever perform this task perfectly. 
Was there enough sophistication in feed forward neural network (with non linear activations) to learn this task?
Would adding an RNN layer make the netowrk [Turing Complete](https://en.wikipedia.org/wiki/Turing_completeness) or does the [Universal Approximation Theorem (UAT)](https://en.wikipedia.org/wiki/Universal_approximation_theorem) mean that a non-recurrent network should be able to learn the task.

UAT is well discussed [here](http://neuralnetworksanddeeplearning.com/chap4.html) and two important caveats are given; approximation and a continuous function - both of which would come into play with this example.

And the difference between the two is discussed [here](https://cs.stackexchange.com/questions/68820/confused-between-turing-completeness-and-universal-approximation-are-they-rela).

To test I added an LSTM layer to provide this memory / loop and improvements are definitely seen - more accurate results showing a greater approximation of Fizzbuzz are seen, getting up to only 1 wrong answer in the entire population vs 7 in the original model.

(Additionally the experiment was made considerably more robust by using an unseen test set after an oversight on my behalf!)


