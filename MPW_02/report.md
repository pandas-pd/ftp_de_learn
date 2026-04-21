# Mandatory Practical Work 02 – 20/04/

## Objective overview

### Main objectives:
- [x] a) Understand the concepts of backpropagation and of forward and backward passes in the context of a computational graph.
- [x] b) Implement new nodes in a computational graph.
- [x] c) Implement a training loop with stochastic and batch approaches
- [x] d) Reimplement and experiment with different optimization algorithms and compare their performance.

### Optional Objectives (chosen):
tbd

### Optional Objectives (available):
- [ ] Investigate the use of 2nd order model instead of the simple linear model
- [ ] Re-implement and experiment with more advanced optimizers such as RMSProp, Nesterov or Adam
- [ ] Implement a Learning Rate Decay on Plateaustrategy in the training loop
- [ ] Normalize the input data with a zero norm approach and compare to your experiments without normalization
- [ ] Implement an early stopping strategy in your training loop

<br>
# Computational graphs and optimizers

Deadline: Monday May 18 ;Format: pdf or ipynb. Clearly state the group members’name
andsurnameat the beginning of the report.


## 1 Overview

Reminder : theMandatory Practical Worksare intended to be done in groups of max 3 stu-
dents. The goal is to apply the concepts seen in the lectures and practical sessions, and to
document your experimentation results in a report. The report should be clear, concise, and
well-structured, including all relevant details about your experiments such as the hyperpara-
meters you used, the results you obtained, and any insights or conclusions you can draw.


## 2 Context

Computational graphs

In this practical work, we will be using a simple computational graph implementation provided
in the filecgnodes.py.

This implementation follows the definition given in the class : a computational graph is adirec-
ted acyclic graphwherenodescorrespond to operations or variables andedgescorrespond
to links between nodes.

Withcgnodes.py, the creation of the graph involves three steps :

a) Creation of the value nodes withValueNode()objects.
b) Creation of the operator nodes with objectsMultiplyNode(),SquareNode()...
c) Build the graph by declaring inputs and outps as 2 lists ofValueNode()objects.
d) Use of the graph with forward and backward calls, e.g.cg.forward(inputs)

Figure 1 shows an example and the code used to implement the graph is given in listing 1.

Figure 1– Simple graph computingf= (x 1 x 2 )^2. The implementation uses operator nodes
(red) and three types of value nodes storing scalar float values : input (yellow), intermediary
(green) and output (blue).

``` python
# first create all ValueNode objects
x1 = ValueNode()
x2 = ValueNode()
q = ValueNode()
f = ValueNode()

 # second create all <Operator>Node objects
mult = MultiplyNode(x1, x2, q)
square = SquareNode(q, f)

# finally build the graph by declaring inputs and outputs as 2 lists of
ValueNode objects
12 cg = CompGraph([x1, x2], [f])
13
14 # test the graph with some random inputs
15 cg.forward([2.0, 4.0])
16 print(f"f = {f.v}") # should print 64.
```


Listing 1 – Simple computational graph example

Regression problem

We will play with a regression problem to predict a valueyfrom input featuresx. The simplest
regression model is a linear model defined with the parametersθas follows :

[add equation here]

Thelosstypically used for regression problems is theMean Square Error(MSE) defined with :

[add equation here]

As illustrated in the python notebook provided for this practical work (and as alredy seen in
practival work week 1), there exist aclosed formsolution to this problem given by the following
normal equation :

[add equation here]

The Eq. 3 allows to compute the “best” θ’s minimising the squared difference between the
gotten outputs and thetargetoutputs defined with Eq. 2. However, this implementation does
not allow to handle large datasets (withN large, matrix inversion becomes more difficult) and
does not allow for incremental learning (fine-tuning) when new data are coming. Therefore we
want now to experiment with abackpropagationstrategy using acomputational graph.

The graph version of Eq. 1 is illustrated on Figure 2.

Figure 2– Computational graph corresponding to the linear regression


## 3 Objectives

It is now time to move to the Python codecdgnodesand notebookscg-linear-regressopm-stud.ipynb
notebook that you need to complete.

Main objectives


a) Understand the concepts of backpropagation and of forward and backward passes in the
context of a computational graph.
b) Implement new nodes in a computational graph.
c) Implement a training loop with stochastic and batch approaches
d) Reimplement and experiment with different optimization algorithms and compare their performance.

Optional objectives

Pick at least 2 of the following optional objectives to further explore and analyze the perfor-
mance of your models :

- [ ] Investigate the use of 2nd order model instead of the simple linear model
- [ ] Re-implement and experiment with more advanced optimizers such as RMSProp, Nesterov or Adam
- [ ] Implement an early stopping strategy in your training loop
- [ ] Implement a Learning Rate Decay on Plateaustrategy in the training loop
- [ ] Normalize the input data with a zero norm approach and compare to your experiments without normalization
