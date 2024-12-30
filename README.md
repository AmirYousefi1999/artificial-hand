clc;
clear;
close all;

% Parameters for thumb
L1t = 45;
L2t = 45;
L3t = 12.5;

% Parameters for finger 1
L1_1 = 30;%20;
L2_1 = 35;%25;
L3_1 = 35;

% Parameters for finger 2
L1_2 = 40;%25;
L2_2 = 40;%30;
L3_2 = 35;

% Parameters for finger 3
L1_3 = 30;%20;
L2_3 = 35;%25;
L3_3 = 35;

% Parameters for finger 4
L1_4 = 25;%15;
L2_4 = 30;%20;
L3_4 = 35;

% Define plotting range
theta_range = 0:pi/100:3*pi/4;
num_points = length(theta_range);

% Create figure
figure;
hold on;
grid on;
axis equal;
xlim([-200 200]);
ylim([-200 200]);
zlim([0 200]);
xlabel('X');
ylabel('Y');
zlabel('Z');
pbaspect([1 1 0.5]);

% Thumb out line bound
alpha1 = pi/3;
alpha2 = 0;
alpha3 = 0;
for i = 1:num_points
    theta1 = theta_range(i);
    Xp_tO = ((L1t + L2t + L3t) * cos(theta1) + L1t * cos(alpha1) + L2t * cos(alpha1 + alpha2) + L3t * cos(alpha1 + alpha2 + alpha3));
    Yp_tO = ((L1t + L2t + L3t) * cos(theta1) + L1t * sin(alpha1) + L2t * sin(alpha1 + alpha2) + L3t * sin(alpha1 + alpha2 + alpha3));
    Zp_tO = L1t + L2t + L3t * sin(theta1)+L1t*sin(theta1);

    plot3(Xp_tO, Yp_tO, Zp_tO, '.');
end

% Thumb in line bound
alpha1 = pi/3;
alpha2 = pi/3;
alpha3 = pi/3;
for i = 1:num_points
    theta1 = theta_range(i);
    Xp_tI = ((L1t + L2t + L3t) * cos(theta1) + L1t * cos(alpha1) + L2t * cos(alpha1 + alpha2) + L3t * cos(alpha1 + alpha2 + alpha3));
    Yp_tI = ((L1t + L2t + L3t) * cos(theta1) + L1t * sin(alpha1) + L2t * sin(alpha1 + alpha2) + L3t * sin(alpha1 + alpha2 + alpha3));
    Zp_tI = L1t + L2t + L3t * sin(theta1)+L1t*sin(theta1);

    plot3(Xp_tI, Yp_tI, Zp_tI, '.');
end

% FINGER 1 out line bound
alpha1 = pi/6;
alpha2 = 0;
alpha3 = 0;
for i = 1:num_points
    theta1 = theta_range(i);
    Xp_1O = 23/2 * ones(size(theta1));
    Yp_1O = ((L1_1 + L2_1 + L3_1) * cos(theta1) + L1_1 * cos(alpha1) + L2_1 * cos(alpha1 + alpha2) + L3_1 * cos(alpha1 + alpha2 + alpha3));
    Zp_1O = ((L1_1 + L2_1 + L3_1) * sin(theta1) + L1_1 * sin(alpha1) + L2_1 * sin(alpha1 + alpha2) + L3_1 * sin(alpha1 + alpha2 + alpha3));

    plot3(Xp_1O, Yp_1O, Zp_1O, '.');
end

% FINGER 1 in line bound
alpha1 = pi/6;
alpha2 = pi/6;
alpha3 = pi/6;
for i = 1:num_points
    theta1 = theta_range(i);
    Xp_1I = 23/2 * ones(size(theta1));
    Yp_1I = ((L1_1 + L2_1 + L3_1) * cos(theta1) + L1_1 * cos(alpha1) + L2_1 * cos(alpha1 + alpha2) + L3_1 * cos(alpha1 + alpha2 + alpha3));
    Zp_1I = ((L1_1 + L2_1 + L3_1) * sin(theta1) + L1_1 * sin(alpha1) + L2_1 * sin(alpha1 + alpha2) + L3_1 * sin(alpha1 + alpha2 + alpha3));

    plot3(Xp_1I, Yp_1I, Zp_1I, '.');
end

% FINGER 2 out line bound
alpha1 = pi/6;
alpha2 = 0;
alpha3 = 0;
for i = 1:num_points
    theta1 = theta_range(i);
    Xp_2O = 36.5 * ones(size(theta1));
    Yp_2O = ((L1_2 + L2_2 + L3_2) * cos(theta1) + L1_2 * cos(alpha1) + L2_2 * cos(alpha1 + alpha2) + L3_2 * cos(alpha1 + alpha2 + alpha3));
    Zp_2O = ((L1_2 + L2_2 + L3_2) * sin(theta1) + L1_2 * sin(alpha1) + L2_2 * sin(alpha1 + alpha2) + L3_2 * sin(alpha1 + alpha2 + alpha3));

    plot3(Xp_2O, Yp_2O, Zp_2O, '.');
end

% FINGER 2 in line bound
alpha1 = pi/6;
alpha2 = pi/6;
alpha3 = pi/6;
for i = 1:num_points
    theta1 = theta_range(i);
    Xp_2I = 36.5 * ones(size(theta1));
    Yp_2I = ((L1_2 + L2_2 + L3_2) * cos(theta1) + L1_2 * cos(alpha1) + L2_2 * cos(alpha1 + alpha2) + L3_2 * cos(alpha1 + alpha2 + alpha3));
    Zp_2I = ((L1_2 + L2_2 + L3_2) * sin(theta1) + L1_2 * sin(alpha1) + L2_2 * sin(alpha1 + alpha2) + L3_2 * sin(alpha1 + alpha2 + alpha3));

    plot3(Xp_2I, Yp_2I, Zp_2I, '.');
end

% FINGER 3 out line bound
alpha1 = pi/6;
alpha2 = 0;
alpha3 = 0;
for i = 1:num_points
    theta1 = theta_range(i);
    Xp_3O = 61.5 * ones(size(theta1));
    Yp_3O = ((L1_3 + L2_3 + L3_3) * cos(theta1) + L1_3 * cos(alpha1) + L2_3 * cos(alpha1 + alpha2) + L3_3 * cos(alpha1 + alpha2 + alpha3));
    Zp_3O = ((L1_3 + L2_3 + L3_3) * sin(theta1) + L1_3 * sin(alpha1) + L2_3 * sin(alpha1 + alpha2) + L3_3 * sin(alpha1 + alpha2 + alpha3));

    plot3(Xp_3O, Yp_3O, Zp_3O, '.');
end

% FINGER 3 in line bound
alpha1 = pi/6;
alpha2 = pi/6;
alpha3 = pi/6;
for i = 1:num_points
    theta1 = theta_range(i);
    Xp_3I = 61.5 * ones(size(theta1));
    Yp_3I = ((L1_3 + L2_3 + L3_3) * cos(theta1) + L1_3 * cos(alpha1) + L2_3 * cos(alpha1 + alpha2) + L3_3 * cos(alpha1 + alpha2 + alpha3));
    Zp_3I = ((L1_3 + L2_3 + L3_3) * sin(theta1) + L1_3 * sin(alpha1) + L2_3 * sin(alpha1 + alpha2) + L3_3 * sin(alpha1 + alpha2 + alpha3));

   

 plot3(Xp_3I, Yp_3I, Zp_3I, '.');
end

% FINGER 4 out line bound
alpha1 = pi/6;
alpha2 = 0;
alpha3 = 0;
for i = 1:num_points
    theta1 = theta_range(i);
    Xp_4O = 86.5 * ones(size(theta1));
    Yp_4O = ((L1_4 + L2_4 + L3_4) * cos(theta1) + L1_4 * cos(alpha1) + L2_4 * cos(alpha1 + alpha2) + L3_4 * cos(alpha1 + alpha2 + alpha3));
    Zp_4O = ((L1_4 + L2_4 + L3_4) * sin(theta1) + L1_4 * sin(alpha1) + L2_4 * sin(alpha1 + alpha2) + L3_4 * sin(alpha1 + alpha2 + alpha3));

    plot3(Xp_4O, Yp_4O, Zp_4O, '.');
end

% FINGER 4 in line bound
alpha1 = pi/6;
alpha2 = pi/6;
alpha3 = pi/6;
for i = 1:num_points
    theta1 = theta_range(i);
    Xp_4I = 86.5 * ones(size(theta1));
    Yp_4I = ((L1_4 + L2_4 + L3_4) * cos(theta1) + L1_4 * cos(alpha1) + L2_4 * cos(alpha1 + alpha2) + L3_4 * cos(alpha1 + alpha2 + alpha3));
    Zp_4I = ((L1_4 + L2_4 + L3_4) * sin(theta1) + L1_4 * sin(alpha1) + L2_4 * sin(alpha1 + alpha2) + L3_4 * sin(alpha1 + alpha2 + alpha3));

    plot3(Xp_4I, Yp_4I, Zp_4I, '.');
end

% Final touches
hold off;
