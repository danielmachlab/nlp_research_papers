# Orca: Progressive Learning from Complex Explanation Traces of GPT-4

[https://arxiv.org/abs/2306.02707](https://arxiv.org/abs/2306.02707)

# Summary:

The objective in this paper is to show how to enhance the capability of smaller models through learning from Large Foundational Models (LFMs) and overcomming the challenges to doing so:

- Shallow LFM outputs when closed-box LFM like GPT-4 don’t show the trace or reasoning of how it arrived to an answer
- Small-scale training data
- Lack of accurate evaluation that overestimates a model’s capability as it learns to imitate the style, but not the reasoning process of LFM

Orca is a model by Microsoft built upon the LLaMA model family using training data consisting of the triple: 

```
(System message, User query, LFM response)
```

********************System message:******************** Instruction to the LFM of what role it is playing, for example:

> You are an AI assistant, that follows instructions extremely well. Help as much as you can.
> 

**********************User query**********************: The actual task for the LFM we want it to perform. For example:

> Which small lake lies between Windermere and Grasmere?
> 
- Different approaches to elicit an explanation were used such as “explain like I’m five”, “think step-by-step”, and “justify your response”

**LFM response**: The response from the LFM when passed the **************system message************** and **********user query********** 

In conclusion, the paper suggests that smaller models can be trained to be more focused and adaptable in more specialized settings to perform in those areas without a substantial loss in quality when compared to a LFM

# Follow-up reading topics

- Vicuna
- LLaMA