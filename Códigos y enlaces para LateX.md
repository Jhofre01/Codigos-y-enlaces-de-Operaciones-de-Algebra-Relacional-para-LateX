   # 1. Operacion Selección
 # 1.1 Codigo de Notación
$$ \sigma_{\text{Predicado}}(R) $$
 # 1.2 Codigo de ecuación de ejemplo
$$ \sigma_{\text{sueldo} \ge 8000 \wedge \text{ingreso} \ge \text{01/01/2003}}(\text{Empleado}) $$

   # 2. Operación Proyección
 # 2.1 Codigo de Notación
$$ \pi_{\text{Lista\_de\_atributos}}(R). $$
 # 2.2 Codigo de ecuacion de ejemplo
$$ \pi_{\text{sueldo, depto}}(\text{Empleado}) $$

   # 3. Operación Unión
 # 3.1 Codigo de Notación
$$ (R \cup S). $$
 # 3.2 Codigo de ecuación de ejemplo
$$ r = \sigma_{\text{sueldo} \ge 10000}(\text{Empleado}) $$
$$ s = \sigma_{\text{depto} = \text{A1}}(\text{Empleado}) $$
$$ \pi_{\text{nombre}}(r \cup s) $$

   # 4. Operación Diferencia
 # 4.1 Codigo de Notación
 $$ R - S $$
 # 4.2 Codigo de ecuación de ejemplo
$$ r = \sigma_{\text{sueldo} \ge 10000}(\text{Empleado}) $$
$$ s = \sigma_{\text{depto} = \text{A2}}(\text{Empleado}) $$
$$ \pi_{\text{nombre},\ \text{sueldo}}(r - s) $$

   # 5. Operación Intersección
 # 5.1 Codigo de Notación
$$ R \cap S = R - (R - S) $$
 # 5.2 Codigo de ecuación de ejemplo
$$ r = \pi_{\text{sueldo}}\bigl(\sigma_{\text{depto}= \text{A1}}(\text{Empleado})\bigr) $$
$$ s = \pi_{\text{sueldo}}\bigl(\sigma_{\text{depto}= \text{A2}}(\text{Empleado})\bigr) $$
$$ r \cap s $$

   # 6. Operacion Producto cartesiano
 # 6.1 Codigo de Notación
$$ R \times S $$
 # 6.2 Codigo de ecuación de ejemplo
$$ \sigma_{\text{depto} = \text{A1}}\bigl(\text{Empleado}\bigr) \times \text{Departamento} $$

   # 7. Operación Join Natural
 # 7.1 Enlace de generación de Notación y Alternativo
https://latex.codecogs.com/png.latex?\dpi{200}\Large\;R\;\bowtie\;S
https://latex.codecogs.com/png.latex?\dpi{200}\Large\;R\;\bowtie\;S\;\equiv\;R\;\times\;S
 # 7.2 Enlace de generación de ecuación de ejemplo
https://latex.codecogs.com/png.latex?\dpi{200}\Large%20\pi_{RFC,nombre,depto,nom\_depto}%20(Empleado%20\bowtie%20Departamento)

   # 8. Operación Theta Join 
 # 8.1 Enlace de generación de Notación
https://latex.codecogs.com/png.latex?\dpi{200}\Large\;R\;\bowtie_{\theta}\;S
 # 8.2 Enlace de generación de ecuación de ejemplo
https://latex.codecogs.com/png.latex?\dpi{200}\Large%20\pi_{RFC,nombre,depto,nom\_depto}\left(Empleado%20\bowtie_{\text{depto}=A2}%20Departamento\right)

   # 9. Operación Join externo
 # 9.1 Enlace de generación de Notación
https://latex.codecogs.com/png.latex?\dpi{200}\Large%20R%20=%20\bowtie_{\theta}%20S%20\mid%20R%20\bowtie=_{\theta}%20S%20\mid%20R%20=%20\bowtie=_{\theta}%20S.

   # 10. Operacion Renombrar
 # 10.1 Codigo de Notación
$$ \rho_{\text{NuevoNombre}}(R) $$
$$ \rho_{\text{NuevoNombre} \leftarrow \text{atributo}}(R) $$
 # 10.2 Codigo de ecuación de ejemplo
$$ \rho_{D}(\text{Departamento}) $$

   # 11. Operacion Agrupación
 # 11.1 Codigo de Notación
$$ \gamma_{\text{atributo\_agrupación} \; ; \; \text{función\_agregación} \rightarrow \text{alias}}(R) $$
 # 11.2 Codigo de ecuación de ejemplo
$$ \gamma_{\text{depto};\ \text{avg(sueldo)} \rightarrow \text{sueldoProm}} (\text{Empleado}) $$

   # 12. Operación Ordenamiento 
 # 12.1 Codigo de Notación
$$ \tau_{\text{atributo1 [asc | desc]},\ \text{atributo2 [asc | desc]},\ \ldots}(R) $$

   # 13. Operación División
 # 13.1 Codigo de Notación
$$ R \div S $$
 # 13.2 Enlace y Codigos de ecuación de ejemplo
https://latex.codecogs.com/png.latex?\dpi{200}\Large\;S\leftarrow\sigma_{\text{sueldo}\le6000}\bigl(\text{Empleado}\;\bowtie\;\text{Departamento}\bigr)
$$ r \leftarrow \pi_{\text{depto},\,\text{sueldo}}(S) $$
$$ \text{Empleado} \div r $$

   # 14. Operaciones de Mantenimiento de datos
 # 14.1.1 Notacion del concepto de Mantenimiento datos (Borrado)
$$ R = R - e $$
 # 14.1.2 Notacion del concepto de Mantenimiento datos (Inserción)
$$ R = R \cup e $$
