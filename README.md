# Network-Based-Model-in-R

A network model is a way of representing the connections between items or people in a group. In the context of infectious diseases, a network model can be used to study how an infectious disease spreads through a population by tracking the movement of infected individuals through the network. Network models can also be used to evaluate the effectiveness of interventions, such as vaccination programs or quarantine measures, in controlling the spread of the disease.

To create a network model using the statnet package in R, you will need to install the package and load it into your R session:

install.packages("statnet")
library(statnet)

Next, you will need to create a matrix or data frame containing your network data. The matrix should contain rows and columns representing the nodes in the network, and the entries in the matrix should indicate whether an edge exists between two nodes. For example, if node 1 is connected to node 2, you would place a 1 in the (1,2) entry of the matrix, and if node 1 is not connected to node 2, you would place a 0 in the (1,2) entry.

Here is an example of how you can create a network data matrix in R:

# Create an empty matrix with 5 rows and 5 columns
mat <- matrix(0, nrow=5, ncol=5)

# Set the entries in the matrix to indicate the presence of edges between nodes
mat[1,2] <- 1
mat[1,3] <- 1
mat[2,3] <- 1
mat[3,4] <- 1
mat[4,5] <- 1

# View the matrix
mat


This will create a matrix with 5 rows and 5 columns, representing a network with 5 nodes. The matrix will contain 1s in the entries (1,2), (1,3), (2,3), (3,4), and (4,5), indicating the presence of edges between these nodes.

Once you have created your network data matrix or data frame, you can use the network function from the statnet package to create a network object:

net <- network(mat, directed=FALSE)
net <- network(mat, directed=FALSE)


Where mat is your network data matrix, and directed=FALSE indicates that the network is undirected (i.e., edges have no direction).

You can then use various functions from the statnet package to analyze and visualize your network model. For example, you can use the plot function to visualize the network:

plot(net, vertex.size=5)


This will create a plot of the network, with nodes represented as circles and edges represented as lines. The size of the nodes can be adjusted using the vertex.size argument.

There are many other functions available in the statnet package for analyzing and visualizing network data. You can find more information about these functions in the package documentation.
