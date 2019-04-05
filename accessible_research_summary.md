# An Introductory Primer To NLP

To be honest, NLP is not really one field, but rather, several different fields which have all converged on the same problem: Language, how does it work?

## Two Camps Within NLP

### Language Is A Series of Symbols

This approach looks at language as the same as any other pattern-recognition problem. Language is a sequence of symbols- sounds, words, sentences, whatever- arranged in specific patterns, and we can find out the patterns via machine if we have enough data for a particular language. This is called the _statistical approach_ to NLP.

With the creation of computers that have enough processing power to run neural networks, *statistical NLP* has evolved into *neural NLP*- using neural nets to recognize patterns in the data. (If you're confused as to what a neural net is, skip down to the `definitions` section!)

### Language Is A Structure With Rules

This is structural linguistics, or as I like to call it, the natural-phenomena approach to linguistics. According to this approach, language is not just a series of symbols, but a complex natural phenomena governed by rules (just like any other natural phenomena), and with careful enough study of language, we can:

- find out the rules that govern language
- Make a working model of how language works
- Program this model into computers

This is called the _rule-based_ approach by people within the field

### Well, They're Not That Separate

In practice, of course, the two approaches are not quite separate. There's a hybrid approach to NLP, which takes the best of both approaches and combines them, but more on that later!

## Why Should You Care About These Approaches?

Well,

I was once asked by my internship supervisor- "What does google have that we don't?" The answer? Data. Tons of it. Unfathomable amounts of it. Enough data that outliers in smaller amounts of data

Which is all well and good- after all, so-called "data science" is the hot thing now. However, it's blindness to assume that we can rely on

Even if we do rely on purely data-based approaches, we should at least make the best of the data we have. Which means creating, evaluating and bit-by-bit improving on the pattern-recognition algorithms we currently have, so that they can

- Extract more information- and more complicated patterns- from the same amount of data
 - Be able to extract the same amount of information from less data. Data collection is expensive, effort-consuming and time-consuming, you see, unless you're a privacy-invading megacorporation with more money than ethics.

(Note: the simpler and less jargon-y name for machine learning is "Pattern Recognition and Statistics- That Uses Lots of Compute Power". No, seriously, there's a machine learning textbook which is just titled "Pattern Recognition")

## Why Should You Care?

### Give A Computer Enough Data (And Processing Power) And It Can Rule The World

Let's put aside the . OpenAI- an AI startup- recently published a paper that, using 40 gigabytes of data and a massive amount of compute power, demonstrated that it could generate- yes, generate- text that was perfectly understandable, and almost eloquent. They gave their machine a prompt, and the machine would generate a paragraph or more in response- all in flawless English.

###

So why am I following this? IIIT has its own GPU cluster- I could collec

(If you're confused as to what a GPU is, once again, skip down to the `Definitions` section!)

Well, first of all, there are flaws with neural


## Definitions

### GPU

("Graphics Processing Unit cluster"- a GPU is a type of specialized CPU that is optimized for being able to process large blocks of data very fast. Initially used for graphics, which requires millions of matrix operations per second. Since machine learning also requires millions of matrix operations per second- machine learning fundamentally relies on matrix math- they've been adopted for machine learning. They're also adopted for other high-processing-power-needed applications, like bitcoin mining.)

### Neural Net

So neural networks- or as the technical name goes, Multilayer Perceptrons- have generated a lot of hype and myth around them.

In truth, neural networks are pretty damn simple as long as you aren't doing the math yourself.

#### Perceptron

Let's start with the founding block of a NN- a perceptron (a "neuron"). A perceptron is a mathematical equation that takes 'n' inputs, runs it through a linear equation, puts the result of that equation through another, nonlinear equation, and gives a single output.

To demonstrate graphically:

[insert image here]

The cool thing about a perceptron is, the linear equation that you're running the inputs through, has _coefficients_ - coefficients that don't have to stay the same, but can be changed by the program. Basically, the equation is of the form ax + by + cz + ... = 0 - your basic linear equation, with as many variables as there are inputs- and a, b, c... are the coefficients, or _parameters_ as they're called technically- which can be changed.

Why do we want to change the parameters? Well, see, we want the perceptron to produce a _specific_ output- the output that we say is correct. Therefore, we don't want any random linear function in the perceptron- we want the _correct_ function, or at least as close to the correct function as we can get. And so we get the "correct" function- or in other words, the set of parameters which give us the least wrong result- by doing the following steps:

(1) For a given set of inputs, letting the function guess the output.
(2) Checking to see if the function's output is close to the actual output
(3) If the function's output is not close to the actual output, we perform some pretty math and change the parameters of the function a little bit, so that (according to our math) the next output the function gives will be closer to the input.

(The nonlinear 'activation function' basically just converts the result of the linear equation to a number in a set- [-1 or +1] in a lot of cases. This is important because with a lot of applications you just want the answer to "is this thing most probably in category A (-1) or category B (+1)?")

#### Neural Net

So now that we know what a perceptron is, we can easily understand what a neural net is. 

A neural set is basically multiple 'layers' of perceptrons, 'stacked' on top of each other such that the output of any one perceptron in the lower layer goes to _all_ the perceptrons in the layer above it.

(In practice, this may not always happen- there are neural net alterations like attention and dropout, that sever some of the connections between layers or skip some layers. That's cool stuff, but a little harder to explain.)







