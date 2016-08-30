function p = predict(Theta1, Theta2, X)
%PREDICT Predict the label of an input given a trained neural network
%   p = PREDICT(Theta1, Theta2, X) outputs the predicted label of X given the
%   trained weights of a neural network (Theta1, Theta2)

% Useful values
m = size(X, 1);
num_labels = size(Theta2, 1);

% You need to return the following variables correctly 
p = zeros(size(X, 1), 1);

% ====================== YOUR CODE HERE ======================
% Instructions: Complete the following code to make predictions using
%               your learned neural network. You should set p to a 
%               vector containing labels between 1 to num_labels.
%
% Hint: The max function might come in useful. In particular, the max
%       function can also return the index of the max element, for more
%       information see 'help max'. If your examples are in rows, then, you
%       can use max(A, [], 2) to obtain the max for each row.
%

X=[ones(m,1) X];

p=zeros(m,1);
%ahcer el forward propagation
for i=1:m
	a1=X(i,:);
	%a1=[a1];  YA LE HABIA AGREGADO EL 1 A a1 CUANDO LE AGREGUE LA COLUMNA DE UNOS A X
	a1=a1';
	z2=Theta1*a1;
	a2=sigmoid(z2);
	a2=[1 ;a2];
	z3=Theta2*a2;
	a3=sigmoid(z3);%h
	[m,ind]=max(a3,[],1); % ME EQUVICOQUE PORQUE ERA 1, NO 2, YA QEU A3 ES COLUMNA NO FILA	
%luego rellenar p
	p(i,1)=ind;
%%%%%%%%%%%%%%%%% HACERLO VECTORIZADO LA RPEDICCION

end

% =========================================================================


end
