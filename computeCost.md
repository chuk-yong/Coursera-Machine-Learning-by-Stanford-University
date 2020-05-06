# Coursera-Machines-Learning-by-Standford-University
## Week 2 Programming - Compute Cost

To get to the solution, I find it helpful to try out the solution on the command panel.  We can do it simply by first following the example in ex1.pdf

```octave
  data = load('ex1data1.txt'); % read comma separated data 
  X = data(:, 1); 
  y = data(:, 2); 
  m = length(y); % number of training examples

  plot(x, y, 'rx', 'MarkerSize', 10); % Plot the data to make sure we have loaded it right
```

From here, we start the calculation.

```octave
  X = [ones(m,1), data(:,1)]; % Add extra rows of 1 to represent theta0. Check in the workspace that it has a dimension of 97x2
  h=X*theta;
  cf = ((h-y).^2)/(2*m); % we now have a column matrix of all the elements
  J = sum(cf); % add up all the elements in the column
```

Enter J in the command will return a value of 32.07


