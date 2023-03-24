Enlista la poblacion de Azcapotzalco y que solo sean hombres

    SELECT * 
    FROM `wifi.poblacion`
    WHERE alcaldia='AZCAPOTZALCO' and sexo='Hombre';

Muestra la alcaldia y la poblacion que este en el rango de edad de 20 a 24 años, que sean mujeres y haya mas de 200000

    SELECT alcaldia, rango_edad,poblacion
    FROM `wifi.poblacion`
    WHERE poblacion  >20000 and rango_edad='e) 20 a 24 años' and sexo='Mujer';

muestra el total de habitantes por alcaldia

    SELECT alcaldia,sum(poblacion) AS suma_por_alcaldia
    FROM `wifi.poblacion`
    GROUP BY(alcaldia);
    
por alcaldia pero solo mujeres en forma descendente

    SELECT alcaldia,sum(poblacion) AS mujeres_por_alcaldia
    FROM `wifi.poblacion`
    WHERE sexo='Mujer' GROUP BY(alcaldia) ORDER BY(alcaldia) DESC;

Enlilista el promedio por alcaldia y ordena de forma ascendente

    SELECT alcaldia, max(poblacion) AS promedio 
    FROM `wifi.poblacion`
    GROUP BY (alcaldia) ORDER BY(MAX(poblacion)) ASC;
    
 muestra el promedio de habitantes por sexo
 
    SELECT sexo,AVG(poblacion)
    FROM `wifi.poblacion`
    GROUP BY(sexo);
    
modificar el  nombre de la alcaldia AZCAPOTZALCO A AZC

    UPDATE `wifi.poblacion`
    SET alcaldia='AZC'
    FROM `wifi.poblacion`
    WHERE alcaldia='AZCAPOTZALCO';
    
MUESTRA LA ALCALDIA QUE TIENE MAS POBLACION
