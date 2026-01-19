# 📊 Análisis de Consultas SQL


## 📈 Resumen
✅ 10 correctas de 23 queries

## ✅ Query 1: Correcto

⏱ Tiempo: 0.39 ms
🔍 No se usó ningún índice en esta consulta.

---

## ✅ Query 2: Correcto

⏱ Tiempo: 0.31 ms
🔍 No se usó ningún índice en esta consulta.

---

## ✅ Query 3: Correcto

⏱ Tiempo: 0.33 ms
🔍 No se usó ningún índice en esta consulta.

---

## ✅ Query 4: Correcto

⏱ Tiempo: 0.32 ms
🔍 No se usó ningún índice en esta consulta.

---

## ❌ Query 5: Incorrecto
```diff
--- 
+++ 
@@ -1,7 +1,7 @@
-id | nombre | cuatrimestre | curso | id_grado
-72.00 | Bases moleculares del desarrollo vegetal | 1.00 | 3.00 | 7.00
-73.00 | Fisiología animal | 1.00 | 3.00 | 7.00
-74.00 | Metabolismo y biosíntesis de biomoléculas | 1.00 | 3.00 | 7.00
-75.00 | Operaciones de separación | 1.00 | 3.00 | 7.00
-76.00 | Patología molecular de plantas | 1.00 | 3.00 | 7.00
-77.00 | Técnicas instrumentales básicas | 1.00 | 3.00 | 7.00
+id | nombre | curso | id_grado
+72.00 | Bases moleculares del desarrollo vegetal | 3.00 | 7.00
+73.00 | Fisiología animal | 3.00 | 7.00
+74.00 | Metabolismo y biosíntesis de biomoléculas | 3.00 | 7.00
+75.00 | Operaciones de separación | 3.00 | 7.00
+76.00 | Patología molecular de plantas | 3.00 | 7.00
+77.00 | Técnicas instrumentales básicas | 3.00 | 7.00
```

⏱ Tiempo: 0.36 ms
✅ Se usó índice(s) en la consulta: id_grado

---

## ❌ Query 6: Incorrecto
```diff
--- 
+++ 
@@ -1,4 +1,4 @@
-apellido1 | apellido2 | nombre | departamento
+apellido1 | apellido2 | nombre | nombre
 Fahey | Considine | Antonio | Economía y Empresa
 Hamill | Kozey | Manolo | Informática
 Kohler | Schoen | Alejandro | Matemáticas
```

⏱ Tiempo: 0.42 ms
✅ Se usó índice(s) en la consulta: PRIMARY,id_departamento, PRIMARY

---

## ✅ Query 7: Correcto

⏱ Tiempo: 0.56 ms
✅ Se usó índice(s) en la consulta: PRIMARY,nif, PRIMARY,id_asignatura,id_curso_escolar, PRIMARY

---

## ✅ Query 8: Correcto

⏱ Tiempo: 0.38 ms
✅ Se usó índice(s) en la consulta: PRIMARY,id_departamento, PRIMARY, id_profesor,id_grado

---

## ❌ Query 9: Error
- **Descripción**: 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'matricula_asignatura.id_curso_escolar = curso_Escolar.id
WHERE curso.escolar.any' at line 5


## ❌ Query 10: Incorrecto
```diff
--- 
+++ 
@@ -1,4 +1,4 @@
-departamento | apellido1 | apellido2 | nombre
+nombre | apellido1 | apellido2 | nombre
 Agronomía | Monahan | Murray | Micaela
 Economía y Empresa | Fahey | Considine | Antonio
 Economía y Empresa | Lemke | Rutherford | Cristina
```

⏱ Tiempo: 0.41 ms
✅ Se usó índice(s) en la consulta: PRIMARY

---

## ✅ Query 11: Correcto

⏱ Tiempo: 0.32 ms
✅ Se usó índice(s) en la consulta: PRIMARY

---

## ✅ Query 12: Correcto

⏱ Tiempo: 0.32 ms
✅ Se usó índice(s) en la consulta: id_departamento

---

## ❌ Query 13: Error
- **Descripción**: 1146 (42S02): Table 'universidad.ppersona' doesn't exist


## ✅ Query 14: Correcto

⏱ Tiempo: 0.30 ms
✅ Se usó índice(s) en la consulta: id_profesor

---

## ✅ Query 15: Correcto

⏱ Tiempo: 0.35 ms
✅ Se usó índice(s) en la consulta: id_departamento, id_asignatura, id_profesor

---

## ❌ Query 16: Incorrecto
```diff
--- 
+++ 
@@ -1,2 +1,2 @@
-total
+COUNT(*)
 12.00
```

⏱ Tiempo: 0.29 ms
🔍 No se usó ningún índice en esta consulta.

---

## ❌ Query 17: Incorrecto
```diff
--- 
+++ 
@@ -1,2 +1,2 @@
-total
+COUNT(*)
 2.00
```

⏱ Tiempo: 0.30 ms
🔍 No se usó ningún índice en esta consulta.

---

## ❌ Query 18: Incorrecto
```diff
--- 
+++ 
@@ -1,4 +1,4 @@
-departamento | total
+nombre | COUNT(*)
 Educación | 3.00
 Informática | 2.00
 Matemáticas | 2.00
```

⏱ Tiempo: 0.34 ms
✅ Se usó índice(s) en la consulta: id_departamento, PRIMARY

---

## ❌ Query 19: Incorrecto
```diff
--- 
+++ 
@@ -1,4 +1,4 @@
-departamento | total
+nombre | COUNT(profesor.id_profesor)
 Informática | 2.00
 Matemáticas | 2.00
 Economía y Empresa | 2.00
```

⏱ Tiempo: 0.32 ms
✅ Se usó índice(s) en la consulta: id_departamento, PRIMARY

---

## ❌ Query 20: Incorrecto
```diff
--- 
+++ 
@@ -1,4 +1,4 @@
-grau | total
+nombre | COUNT(asignatura.id)
 Grado en Ingeniería Informática (Plan 2015) | 51.00
 Grado en Biotecnología (Plan 2015) | 32.00
 Grado en Ingeniería Agrícola (Plan 2015) | 0.00
```

⏱ Tiempo: 0.33 ms
✅ Se usó índice(s) en la consulta: id_grado

---

## ❌ Query 21: Incorrecto
```diff
--- 
+++ 
@@ -1,2 +1,2 @@
-grau | total
+nombre | COUNT(asignatura.id)
 Grado en Ingeniería Informática (Plan 2015) | 51.00
```

⏱ Tiempo: 0.33 ms
✅ Se usó índice(s) en la consulta: id_grado

---

## ❌ Query 22: Incorrecto
```diff
--- 
+++ 
@@ -1,4 +1,4 @@
-grau | tipo | total_creditos
+nombre | tipo | SUM(asignatura.creditos)
 Grado en Ingeniería Informática (Plan 2015) | básica | 72.00
 Grado en Ingeniería Informática (Plan 2015) | obligatoria | 54.00
 Grado en Ingeniería Informática (Plan 2015) | optativa | 180.00
```

⏱ Tiempo: 0.35 ms
✅ Se usó índice(s) en la consulta: id_grado, PRIMARY

---

## ❌ Query 23: Error
- **Descripción**: 'NoneType' object is not iterable

