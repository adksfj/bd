```sql

-- INNER JOIN
SELECT * FROM Tabla_1 Alias_1 INNER JOIN Tabla_2 Alias_2 ON Alias_1.COLUMNA = Alias_2.COLUMNA;

-- Vistas
CREATE VIEW Nombre_Vista
AS

SELECT FROM WHERE;

SELECT * FROM Nombre_Vista;

-- Funciones agregadas

SELECT AVG(Columna_Tabla) FROM Nombre_Tabla;
SELECT MAX(Columna_Tabla) FROM Nombre_Tabla;
SELECT MIN(Columna_Tabla) FROM Nombre_Tabla;

-- Funciones propias (Funcion escalar)

CREATE FUNCTION NombreFuncion (@Par1 TIPO, @Par2 TIPO)
RETURN TipoDeDatoDevolver
AS
BEGIN

DECLARE @VAR1 TIPO;

SELECT @VAR1 = () FROM TABLA WHERE CONDICION;

RETURN @VAR1;

END

SELECT COLUMNA AS ALIAS, dbo.NombreFuncion(PAR1, PAR2) FROM TABLA WHERE CONDICION;

-- Trigger

CREATE TRIGGER nombre_trigger  
ON tabla  
AFTER INSERT, UPDATE, DELETE  
AS  
BEGIN  
-- lógica automática  
END;


-- Subconsultas

SELECT nombre  
    FROM empleados  
    WHERE salario > (SELECT AVG(salario) FROM empleados);


```
