[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11974275&assignment_repo_type=AssignmentRepo)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$  

Let's begin by subbing in our two F(n) expressions to the formal definition of $O$:  

$T(n) \in O(log_5(n)) \iff \exists c, n_0: T(n) \leq c \cdot (log_5(n)) \forall n \geq n_0$  
                                        &  
$T(n) \in O(log_3(n)) \iff \exists c, n_0: T(n) \leq c \cdot (log_3(n)) \forall n \geq n_0$  

Utilizing the change of base formula for logs, we get the following:  

$T(n) \in O(log_3(n)) \iff \exists c, n_0: T(n) \leq c/(log_5(3)) * log_5(n) \forall n \geq n_0$  
                                        &  
$T(n) \in O(log_3(n)) \iff \exists c, n_0: T(n) \leq d * log_5(n) \forall n \geq n_0$  

Where d represents any arbitrary constant.  

We see something similar shake out for our $log_5$ expressions as well:  

$T(n) \in O(log_5(n)) \iff \exists c, n_0: T(n) \leq c/(log_3(5)) * log_3(n) \forall n \geq n_0$  
                                        &  
$T(n) \in O(log_5(n)) \iff \exists c, n_0: T(n) \leq d * log_3(n) \forall n \geq n_0$  

Where d represents any arbitrary constant.  

Through this, we have effectively shown that $T(n) \in O(log_5(n))$ and T(n) \in O(log_3(n)). Expressed symbolically:  

$\forall T(n) \in O(log_3(n))$  
$T(n) \in O(log_5(n))  
________________________    

$\forall T(n) \in O(log_5(n))$   
$T(n) \in O(log_3(n))$  
