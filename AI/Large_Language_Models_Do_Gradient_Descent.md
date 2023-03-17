# Large Language Models do Gradient Descent at runtime.

In [Why Can GPT Learn In-Context? Language Models Secretly Perform Gradient Descent as Meta-Optimizers](https://arxiv.org/abs/2212.10559), researchers investigate how large language models (LLMs) can perform tasks such as classification from examples given as the "context".

The way this works is you give the model some example sentences and the output (eg "{This is a positive sentence}, {sentiment: positive}") as the context and then give it some unclassified sentences and it will output the sentiment.

This is known as "in-context learning" (ICL) and was a surprising capability of LLMs when first discovered. 

For those who believe LLMs are just "stochastic parrots" that just output what they have read this behavior should be impossible. Typically proponents of this view make objections like "oh it has seen those examples somewhere before", but these are easily disproved by making up your own examples. 

So how is it working?

In this paper the researchers probe the transformer state of the LLM before and after the context examples are loaded and show that the updated transformer state is similar to a large language model that has been fine tuned on the examples(!)

This is a pretty astonishing insight and raises questions about what else LLMs can do. 

It also shows the significant difference between the *training objective* of a language model (just predict the next token) and the capabilities and representation that these models learn. 

To quote the conclusion:

> Further, we build connections between ICL and a specific finetuning setting and find that it is reasonable to regard ICL as a kind of implicit finetuning. Empirically, in order to support our understanding that ICL performs implicit finetuning, we comprehensively compare the behavior of ICL and finetuning based on real tasks. The results prove that ICL behaves similarly to explicit finetuning at the prediction level, the representation level, and the attention behavior level. 

Exactly how LLMs have learned to do this in context learning is a mystery. Obviously compression is forcing a compact form of knowledge representation, but what makes it able to update this repsentation and then use it so easily is certianly surprising.

These experiments were performed on comparativly small models (GPT 1.3B and 2.7B). It would be interesting to see the same experiments performed on models with larger parameter counts. 