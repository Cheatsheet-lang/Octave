# Octave Cheatsheet

### General Commands
```octave
PS1("custom>> ");        % For the Custom prompt

a = 3;      % The semi-colon supresses the output
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