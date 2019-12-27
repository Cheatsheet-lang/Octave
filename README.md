# Octave Cheatsheet

### General Commands
```octave
PS1("custom>> ");        % For the Custom prompt

a = 3;      % The semi-colon supresses the output

help(eye)   % Gives some description about the eye function
who         % Displays all the variables in the scope
whos        % Gives the detailed display of variables

clear a     % Deletes the variable a
save variable.mat a;    % Saves the variable a in the file
save variable.txt a -ascii;    % Saves the variable a in human readable
```

## Basic Operations

#### Variables
```octave
a = 3;
b = 'hi';
```

#### Output
```octave
a  = pi;
a           % Simply give at the prompt
disp(a);    % print function in octave
disp(sprintf('Vaue of pi is: %0.2f', a))        % C style printing
```

#### Arthimetic Operations
```octave
5 + 6
5 - 4
5 * 8
1 / 2
2 ^ 6       % Exponentation
```

#### Logical Opeartions
```octave
1 == 2      % false
1 ~= 2      % not equal to
1 && 0      % AND
1 || 0      % OR
xor(1, 0)
```

## Vectors and Matrices

#### Vectors
```octave
row = [1, 2, 3]     % Row vector , is a separator in a row

col = [1; 2; 3]     % Column vector ; separates the rows

length(row)         % Gives the length of vector/ length of longest dimension in matrix
```

#### Matrices
```octave
matrix = [1, 2; 3, 4; 5, 6]
eye(3)          % Diagonal matrix of order 3
ones(2, 3)      % [1, 1, 1; 1, 1, 1]
zeros(1, 3)     % [0, 0, 0]
mat = rand(3, 2)    % A random 3x2 matrix
randn(1, 100)   % Random matrix following a normal distribution

size(matrix)    % Gives the dimensions of the matrix as a matrix[row, column] size(<matrix>, [axis])

matrix(3, 2)    % A usual matrix indexing
matrix(:,2)     % : means all the elements in the corrsponding row/column.
matrix([1 3],:) % Everything from the 1st and 3rd row

matrix = [matrix, [7; 8; 9]]   % Appending a row to the matrix(right side)
matrix(:, 3) = [10; 11; 12]    % Assiging a row
matrix(:)       % Put all the elements into a single column vector

mat_concat = [matrix mat]   % Concatenate matrices side by side [matrix, mat]
mat_concat = [matrix; mat]  % Concatenate matrices one above the other
```

#### Iterators
```octave
v = 1:0.1:2     % Start:step-size:end deafult step-size is 1
```

## Plotting
```octave
hist(randn(1, 100))     % Plots a histogram hist(<vector>, [bins])
```