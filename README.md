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
