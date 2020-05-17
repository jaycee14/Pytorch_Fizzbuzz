# Pytorch_Fizzbuzz
Recreation (overkill!) of Fizzbuzz in Pytorch

## Rationale

I wanted a small self contained project to help my understanding of Pytorch.
Joel Grus's [excellent blog post](https://joelgrus.com/2016/05/23/fizz-buzz-in-tensorflow/) was the source of this idea and is highly worth a read. I've even borrowed some of his functions.

The classic [Fizzbuzz](https://en.wikipedia.org/wiki/Fizz_buzz) problem can be solved imperically in a few lines of code so creating a neural network is a total overkill but its still a very interesting small project when learning the details of a designing a network, deploying to a GPU and a chance to dig into the basics. 

It's also still powerful to show a pattern being learnt with data alone. 

## Update

I demo'd this to my AI study group - more as a pytorch demo - it kicked off a conversation about whether a simple DNN could ever perform this task perfectly. Was there enough sophistication in feed forward neural network (with non linear activations) to learn, effectively division. There was a view that adding a loop to the network would enable it to better learn the function. To test I added an LSTM layer to provide this 'memory' / loop and at the same time make the experiment more robust with an unseen test set.
Whilst not perfect results there were substanial improvements. 

