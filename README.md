## Notation  
  
$r(i,j)$  :  scalar; = 1 if user j rated game i = 0 otherwise                          
$y(i,j)$  :  scalar; = rating given by user j on game i (if r(i,j) = 1 is defined)	  
$\mathbf{w}^{(j)}$ : vector; parameters for user j                                   
$b^{(j)}$  :  scalar; parameter for user j                                          
$\mathbf{x}^{(i)}$  :  vector; feature ratings for movie i                          
$n_u$  :  number of users  (Python : num_users)  
$n_m$  :  number of movies (Python : num_movies)  
$\mathbf{X}$  :   matrix of vectors $\mathbf{x}^{(i)}$  (Python : X)      
$\mathbf{W}$  :  matrix of vectors $\mathbf{w}^{(j)}$  (Python : W)  
$\mathbf{b}$  :  vector of bias parameters $b^{(j)}$   (Python : b)    
$\mathbf{R}$  :  matrix of elements $r(i,j)$   (Python : R)  
  
  
## Recommender Systems  
  
The goal of a collaborative filtering recommender system is to generate two vectors: For each user, a 'parameter vector' that embodies the movie tastes of a user. For each movie, a feature vector of the same size which embodies some description of the movie. The dot product of the two vectors plus the bias term should produce an estimate of the rating the user might give to that movie.
  
  
## Movie Ratings Dataset  
  
The data set is derived from the [MovieLens "ml-latest-small"](https://grouplens.org/datasets/movielens/latest/) dataset.   
[F. Maxwell Harper and Joseph A. Konstan. 2015. The MovieLens Datasets: History and Context. ACM Transactions on Interactive Intelligent Systems (TiiS) 5, 4: 19:1–19:19. <https://doi.org/10.1145/2827872>]

The original dataset has  9000 movies rated by 600 users. The dataset has been reduced in size to focus on movies from the years since 2000. This dataset consists of ratings on a scale of 0.5 to 5 in 0.5 step increments. The reduced dataset has $n_u = 443$ users, and $n_m= 4778$ movies  
  
  
## Collaborative filtering learning algorithm  
  
The collaborative filtering algorithm in the setting of movie
recommendations considers a set of $n$-dimensional parameter vectors
$\mathbf{x}^{(0)},...,\mathbf{x}^{(n_m-1)}$, $\mathbf{w}^{(0)},...,\mathbf{w}^{(n_u-1)}$ and $b^{(0)},...,b^{(n_u-1)}$, where the
model predicts the rating for movie $i$ by user $j$ as
$y^{(i,j)} = \mathbf{w}^{(j)}\cdot \mathbf{x}^{(i)} + b^{(i)}$ . Given a dataset that consists of
a set of ratings produced by some users on some movies, we wish to
learn the parameter vectors $\mathbf{x}^{(0)},...,\mathbf{x}^{(n_m-1)}, \mathbf{w}^{(0)},...,\mathbf{w}^{(n_u-1)}$  and $b^{(0)},...,b^{(n_u-1)}$ that produce the best fit (minimizes
the squared error).
