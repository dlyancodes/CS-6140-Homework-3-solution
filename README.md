# CS-6140-Homework-3-solution

Download Here: [CS 6140 Homework 3 solution](https://jarviscodinghub.com/assignment/cs-6140-homework-3-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

1. PCA Objective Value. Show that for the optimal solution of fitting a d-dimensional subspace
to data using PCA, the objective function value is equal to P
i≥d+1 σ
2
i
. Here, σi denotes the ith largest singular value of the mean subtracted data matrix, Y¯ =

y1 − y¯ · · · yN − y¯

, where
y¯ =
1
N
PN
i=1 yi
.
2. Locally Linear Embedding. As discussed in the class, the first step of LLE involves solving
the optimization
min
wi
1
2
kY iwik
2
2
s.t. 1
>wi = 1,
where Y i =

· · · yj − yi
· · ·
for all j’s that are neighbors of point j and 1 is a vector of all
1’s of appropriate dimension. a) Prove that the solution of this optimization is given by wi =
(Y
>
i Y i)−11
1>(Y
>
i Y i)−11
. b) Assume that we have N data points in the D-dimensional ambient space. We set
the number of nearest neighbors in LLE to be K. We try to find a d-dimensional representation of
the data. What is the computational cost of step 1 and step 2 of LLE, in terms of big O notation
(for example, O(DpNq
))? Explain your answer in details.
3. Laplacian Matrix. The Laplacian matrix of a graph on N nodes is defined by L = D −
W, where W is the matrix of weights of the graph, where Wij is the weight between nodes i
and j. The degree matrix D is also defined as a diagonal matrix whose i-th diagonal entry is
the sum of the weights of the nodes connected to node i, i.e., Dii =
PN
j=1 Wij . a) Let x =

x1 · · · xN
>
. Compute a closed-form expression for x
>Lx that only depends on Wij ’s. b)
Show that the Laplacian matrix is a positive semi-definite matrix. c) Is L an invertible matrix?
Prove. d) How many zero singular values does L have?
4. Neural Network. Consider a neural net for a binary classification which has one hidden layer
as shown in the figure below. We use a linear activation function a(z) = cz at hidden units and a
sigmoid activation function a(z) = 1/(1 + e
−z
) at the output unit to learn the function for P(y =
1|x, w) where x = (x1, x2) and w = (w1, w2, . . . , w9). A) What is the output P(y = 1|x, w) from
the above neural net? Express it in terms of xi
, c and weights wi
. What is the final classification
boundary? B) Draw a neural net with no hidden layer which is equivalent to the given neural net,
and write weights w˜ of this new neural net in terms of c and wi
. C) Is it true that any multilayered neural net with linear activation functions at hidden layers can be represented as a neural
net without any hidden layer? Explain your answer.
1
4. PCA Implementation. Implement the PCA and the Kernel PCA algorithm. The input to the
PCA algorithm must be the input data matrix Y ∈ R
D×N , where D is the ambient dimension
and N is the number of points, as well as the dimension of the low-dimensional representation,
d. The output of the PCA must be the basis of the low-dimensional subspace U ∈ R
D×d
, the
mean of the subspace µ ∈ R
D and the low-dimensional representations X ∈ R
d×N . For KPCA,
the input must be the Kernel matrix K ∈ R
N×N , where N is the number of points, as well as
the dimension of the low-dimensional representation, d. The output of KPCA must be the lowdimensional representations X ∈ R
d×N .
5. Kmeans Implementation. Implement the Kmeans algorithm. The input to the algorithm
must be the data matrix X ∈ R
D×N , the desired number of clusters, k, as well as the number of
repetitions of kmeans with different random initializations, r. The output of the algorithm must be
the clustering of the data (indices of points in each group) for the best run of the kmeans, i.e., the
run of kmeans that achieves the lowest cost function among all different initializations.
6. Spectral Clustering Implementation. Implement the Spectral Clustering algorithm. The input
to the algorithm must be the similarity matrix W ∈ ReN×N , where Wij is the similarity between
point i and j, and the desired number of clusters, k. The output of the algorithm must be the
clustering of data (indices of points in each group).
7. Testing Algorithms on Data.
Part A. Take the dataset1, which consists of 200 points in 40-dimensional space (Y is 40 × 200
dimensional matrix).
i) Plot the data by using the first and second features (i.e., first and second rows) of Y . Can you
see any structure in data? Explain.
ii) Plot the data by using the second and third features (i.e., first and third rows) of Y . Can you see
any structure in data? Explain.
iii) Apply PCA to data and reduce the dimension of data to d = 2. Your output should be a 2×200
dimensional matrix. Plot the 2-dimensional representation of data using PCA. Can you see any
structure in data? Explain.
iv) Apply Kmeans to the 40-dimensional data. Decide about K based on the PCA plot of the data.
2
Show the results by plotting the 2-dimensional data and indicating data in each cluster by a different color. Explain why Kmeans is or is not successful in recovering the true clustering/grouping of
the data.
v) Apply Kmeans to the 2-dimensional data. Decide about K based on the PCA plot of the data.
Show the results by plotting the 2-dimensional data and indicating data in each cluster by a different color. Explain why Kmeans is or is not successful in recovering the true clustering/grouping of
the data.
vi) Explain the similarities and differences of results between part iv and v? Looking at the plots,
how much the results for applying Kmeans to 40-dimensional original data differ from the results
of applying Kmeans to 2-dimensional representations of data? For general problems, is there any
advantage of first applying PCA and then Kmeans to data?
Part B. Take the dataset2, which consists of 200 points in 40-dimensional space (Y is 40 × 200
dimensional matrix).
i) Plot the data by using the first and second features (i.e., first and second rows) of Y . Can you
see any structure in data? Explain.
ii) Plot the data by using the second and third features (i.e., first and third rows) of Y . Can you see
any structure in data? Explain.
iii) Apply PCA to data and reduce the dimension of data to d = 2. Your output should be a 2×200
dimensional matrix. Plot the 2-dimensional representation of data using PCA. Can you see any
structure in data? Explain.
iv) Apply Kmeans to the 2-dimensional data obtained by PCA. Show the results by plotting the
2-dimensional data and indicating data in each cluster by a different color. Explain why Kmeans
is or is not successful in recovering the true clustering/grouping of the data.
v) Repeat part iv by applying Kernel PCA to data to reduce the dimension of original data to
2. For KPCA, use Gaussian kernel (kij = e
−kyi−yjk
2
2
/(2σ
2
)
) and try several values of σ (Hint:
2-dimensional PCA plots can help you to pick relatively good σ values). Show the results (for
the best σ you could find) by plotting the 2-dimensional data and indicating data in each cluster
by a different color. Explain why KPCA is or is not successful in recovering the true clustering/grouping of the data.
vi) Repeat part iv by applying Spectral to data to reduce the dimension of original data to 2. For
spectral clustering, connect each point to its K nearest neighbors using Euclidean distance between
points and for any two points i and j connected, set the weights to be wij = e
−kyi−yjk
2
2
/(2σ
2
)
. Try
several values of K and σ (Hint: 2-dimensional PCA plots can help you to pick relatively good K
and σ values). Show the results (for the best K and σ you could find) by plotting the 2-dimensional
data and indicating data in each cluster by a different color. Explain why Spectral Clustering is or
is not successful in recovering the true clustering/grouping of the data.
3
Homework Submission Instructions:
– Submission of Written Part: You must submit your written report in the class BEFORE CLASS
STARTS. The written part, must contain the plots and results of running your code on the provided
datasets.
–Submission of Code: You must submit your Python code (.py file) via email, BEFORE CLASS
STARTS. For submitting your code, please send an email to me and CC both TAs.
– The title of your email must be “CS6140: Code: HW3: Your First and Last Name”.
– You must attach a single zip file to your email that contains all python codes and a readme file
on how to run your files.
– The name of the zip file must be “HW3-Code: Your First and Last Name”.

