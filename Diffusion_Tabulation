% 3d_400c

hardness = 0.000000;
time = 3600;
temp = 673;
D0 = 0.003183;
Ea = 154119.13;
R = 8.3145;
Co = 33.9;

% X axis for depth
xaxis=[];
x2axis=[];
x3axis=[];
% Y axis for Concentration
yaxis=[];
y2axis=[];
y3axis=[];
% Z axis for Diffussion
zaxis=[];
z2axis=[];
z3axis=[];

for time=time:3600:10800
    for i=hardness:0.000002:0.000120
        % Formulae Diffusion_coefficient
        D = D0*exp(-Ea/(R*temp));
        % Formulae erf
        erf = i/sqrt(4*D*time);
        % concentration
        concentration = Co*erfc(erf);
        if time == 3600
            xaxis=[xaxis i+i];
            yaxis=[yaxis i+concentration];
            zaxis=[zaxis i+D];
            plot3(xaxis,yaxis,zaxis);
            hold on;
        elseif time == 7200
            x2axis=[x2axis i+i];
            y2axis=[y2axis i+concentration];
            z2axis=[z2axis i+D];
            plot3(x2axis,y2axis,z2axis);
            hold on;
        elseif time == 10800
            x3axis=[x3axis i+i];
            y3axis=[y3axis i+concentration];
            z3axis=[z3axis i+D];
            plot3(x3axis,y3axis,z3axis);
            hold on;
        end
    end
end

title('Concentration of Nitrogen vs Depth vs Diffusion');
xlabel('Depth (M)');
ylabel('Concentration of Nitrogen (mol/dm3)');
zlabel('Diffusion');