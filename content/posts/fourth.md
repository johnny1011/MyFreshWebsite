+++
title = 'Fourth'
date = 2024-10-09T10:26:07+01:00
draft = true
+++


Lecture 5 

In the fifth lecture of LLM agents, Omar Khattab from DSPy discusses LM systems. "What are LM systems?" I hear you asking.

main weakness of LLM, due to the floweter of the models it is hard to know when there are give incorrect tokens,

Ai demons are amazing and easy to build but to make them more rebuest its 

it is incredibly easy to build ai demos , turn monolithic LLM into Liable AI systems. 


compound AI systems are a way people are build to over some these problems. 
-- RAG - Retrieval Augmented Generation
-- -- 
mulit-hot retrieval augmented generation
-- 
STORM: Assisting in Writing Wikipedia-like Articles From Scratch with Large Language Models (Shao et al., 2024)
 -- 

compound AI systems are greate they give use
-1 Quality. 
-2 control 
-3 transparency 
-4 infease Time scaling. 

10 of kd of string to compounds these systems 
each prompt couple five very diffferent roles 
1. The core input → output behavior, a Signature.
2. The computation specializing an inference-time strategy to the signature, a Predictor.
3. The computation formatting the signature's inputs and parses its typed outputs, an Adapter.
4. The computations defining objectives and constraints on behavior, Metrics and Assertions.
5. The strings that instruct (or weights that adapt) the LM for desired behavior, an Optimizer.

could you give the system, 
it needs to 99.9% corrent and its test lots of different prompts, to get that 99.9% correct. test on diffferen modles differnent promots

DSPy is a system that allows you to do this. 
Lm programe f():x -> y x,y in natural languge. 
in the couse of the exexution f() makes calls to modules (m1, ...m3 )

e.g 
fact_checking = dspy.Chain0fThought ( 'claims -> verdicts: list [bool]')
fact_checking(claims=["Python was released in 1991.", "Python is a compiled language."])
Prediction(reasoning='The first claim states that "Python was released in 1991," which is true.Python was indeed first released by Guido van Rossum in February 1991. The second claim states that "Python is a compiled language." This is false; Python is primarily an interpreted language, although it can be compiled to bytecode, it is not considered a compiled language in the traditional sense like C or Java.',
verdicts=[True, False]
)

for each module you can call 