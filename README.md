# Artificial-intelligence-AND NOT FUNCTIONING IN MC Culloch Pitts 

%AND function using McCulloch-Pitts Neuron
clc
clear all
%close all
%Getting weights & Threshold value
disp('Enter the weights');
w1 = input('Weight w1=');
w2 = input('Weight w2=');
disp('Enter the Threshold value');
theta = input('Theta=');
 
y = [0 0 0 0];%initialize to avoid garbage value
x1 = [0 0 1 1];%Input1
x2 = [0 1 0 1];%input2
z = [0 0 0 1];%ideal output

zin = x1*w1+x2*w2;
for i=1:4
    if zin(i)>=theta
        y(i)=1;
    else y(i)=0;
    end
end
disp('Output of net=');
disp(y);
if y==z
    disp('Net is Learning properly');
else
    disp('Net is not Learning properly');
end






%NOT function using McCulloch-Pitts Neuron
clc
clear all
%close all
%Getting weights & Threshold value
disp('Enter the weights');
w1 = input('Weight w1=');
disp('Enter the Threshold value');
theta = input('Theta=');
 
y = [0 0];%initialize to avoid garbage value
x1 = [0 1];%Input1
z = [1 0];%ideal output
 
zin = x1*w1;
for i=1:2
    if zin(i)>=theta
        y(i)=0;
    else y(i)=1;
    end 
end
disp('Output of net=');
disp(y);
if y==z
    disp('Net is Learning properly');
else
    disp('Net is not Learning properly');
end
