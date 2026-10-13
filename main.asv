Ra = 2;        
Kt = 0.01;    
b  = 0.0012;  
La = 0.023;   
Ke = 0.01;     
J  = 0.001;    

Va = 1; 
tspan = [0 0.5];
y0 = [0; 0]; 
sys = @(t,y) [
    (-Ra/La)*y(1) - (Ke/La)*y(2) + (1/La)*Va;
    (Kt/J)*y(1) - (b/J)*y(2)
    ];
[t, y] = ode45(sys, tspan, y0);
figure;
subplot(2,1,1);
plot(t, y(:,1), 'b', 'LineWidth', 1.5);
title('Corriente de Armadura (i_a)');
xlabel('Tiempo (s)'); ylabel('Corriente (A)'); grid on;
subplot(2,1,2);
plot(t, y(:,2), 'r', 'LineWidth', 1.5);
title('Velocidad Angular (\omega_m)');
xlabel('Tiempo (s)'); ylabel('Velocidad (rad/s)'); grid on;