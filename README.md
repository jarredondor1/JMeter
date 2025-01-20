# Proyecto: Pruebas de Rendimiento con JMeter

Este proyecto contiene las pruebas de rendimiento realizadas utilizando Apache JMeter. El propósito es evaluar la capacidad y estabilidad del sistema bajo diferentes condiciones de carga.

## **Descripción del Proyecto**
Las pruebas se llevaron a cabo para validar el desempeño de las siguientes páginas del sistema:
1. `/wiki/Wikipedia:Portada`
2. `/wiki/Portal:Comunidad`
3. `/wiki/Portal:Actualidad`
4. `/wiki/Especial:P%C3%A1ginasNuevas`
5. `/wiki/Sin_miedo_a_nada`

### **Objetivos de las pruebas**
- Validar la estabilidad del sistema bajo 50 usuarios concurrentes durante 5 minutos.
- Evaluar métricas clave como:
  - **Tiempos de respuesta promedio**
  - **Throughput**
  - **Errores**
  - Percentiles clave (90%, 95%, 99%)
- Identificar posibles cuellos de botella.

---

## **Resultados**

### Resumen de las Pruebas
| Página                   | Promedio (ms) | Mínimo (ms) | Máximo (ms) | Throughput (req/s) | Error % |
|--------------------------|---------------|-------------|-------------|---------------------|---------|
| Wikipedia:Portada        | 937           | 96          | 11797       | 8.1                 | 0%      |
| Portal:Comunidad         | 1446          | 188         | 8454        | 8.1                 | 0%      |
| Portal:Actualidad        | 1151          | 104         | 6630        | 8.1                 | 0%      |
| Especial:Páginas Nuevas  | 1600          | 480         | 7131        | 8.0                 | 0%      |
| Sin miedo a nada         | 775           | 87          | 16146       | 8.0                 | 0%      |
| **Total**                | 1182          | 87          | 16146       | 40.1                | 0%      |

---

### **Recomendaciones**
1. **Optimizar Backend**: Reducir tiempos máximos elevados, como los observados en `/wiki/Sin_miedo_a_nada`.
2. **Cacheo**: Implementar estrategias de cacheo para mejorar el rendimiento de `/wiki/Especial:P%C3%A1ginasNuevas`.
3. **Pruebas adicionales**: Escalar la carga de usuarios para evaluar la capacidad máxima del sistema.

---

## **Estructura del Proyecto**
- **Archivos de pruebas (`.jmx`)**:
  - `Reto de Pruebas de Performance.jmx`
- **Reportes**:
  - `aggregate.csv`
  - `summary.csv`
- **Gráficas**:
  - `Graph Results.png`
  - `Summary Report.png`
  - `View Results in Table.png`

---

## **Herramientas Utilizadas**
- **Apache JMeter 5.6.3**: Para la creación y ejecución de las pruebas de rendimiento.
- **Visual Studio Code**: Para el desarrollo y documentación.
- **Git y GitHub**: Para el control de versiones y almacenamiento de los reportes y scripts de prueba.

---

### **Cómo Ejecutar las Pruebas**
1. Clona este repositorio:
   ```bash
   git clone https://github.com/jarredondor1/JMeter.git