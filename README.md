>> % Definir el rango para x, y, z
>> [x, y] = meshgrid(-2:0.1:2);
>> % Definir los planos
>> z1 = (6 - 1.00*x - 2.00*y) / 3.00;
>> z2 = (6.04 - 1.01*x - 2.01*y) / 3.02;
>> z3 = (5.96 - 0.99*x - 1.99*y) / 2.98;
>> % Crear la figura
>> figure;
>> % Graficar los planos
>> surf(x, y, z1, 'FaceAlpha', 0.5, 'EdgeColor', 'none', 'FaceColor', 'b');
>> hold on;
>> surf(x, y, z2, 'FaceAlpha', 0.5, 'EdgeColor', 'none', 'FaceColor', 'r');
>> surf(x, y, z3, 'FaceAlpha', 0.5, 'EdgeColor', 'none', 'FaceColor', 'g');
>> % Configurar el gráfico
>> xlabel('x');
>> ylabel('y');
>> zlabel('z');
>> title('Sistema mal condicionado 3x3');
>> legend('1.00x + 2.00y + 3.00z = 6.00', '1.01x + 2.01y + 3.02z = 6.04', '0.99x + 1.99
y + 2.98z = 5.96');
>> % Ajustar la vista
>> view(30, 30);
>> grid on;
>> axis tight;
>> % Mostrar el punto de intersección teórico
>> hold on;
>> plot3(1, 1, 1, 'ko', 'MarkerSize', 10, 'MarkerFaceColor', 'k');
>> text(1, 1, 1, '  Intersección teórica', 'VerticalAlignment', 'bottom');
>> hold off;
