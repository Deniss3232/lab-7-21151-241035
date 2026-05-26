# RetailMax — Lab 7: Visualización de Datos

---

## Área de negocio: Operaciones y Logística

Este dashboard analítico fue construido para el área de Operaciones y Logística de RetailMax, responsable de garantizar la disponibilidad de productos en tienda, gestionar el inventario y coordinar la relación con proveedores. Los indicadores diseñados permiten monitorear el estado del inventario en tiempo real e identificar riesgos de desabastecimiento y problemas con proveedores.

---

## Integrantes

| Nombre | Carné |
|--------|-------|
| Dally Ramírez| 241035 |
| Denis Rodríguez | 21151 |


---

## Video de presentación



---

## Estructura del repositorio

```
├── docker-compose.yml       # Ambiente completo con PostgreSQL y Metabase
├── DDL.sql                  # Definición de tablas y esquema
├── DATA.sql                 # Datos de prueba precargados
├── metabase-data/           # Volumen persistido con el dashboard construido
├── informe.pdf              # Documentación completa de los 12 indicadores
└── README.md                
```

---

## Instrucciones para levantar el ambiente

El ambiente es completamente reproducible. Solo necesitas Docker instalado.

```bash
git clone https://github.com/Deniss3232/lab-7-21151-241035.git
cd lab-7-21151-241035
docker compose up
```

Espera a que aparezca en los logs el mensaje `Metabase Initialization COMPLETE`, luego abre tu navegador en:

```
http://localhost:3000
```

Ingresa con las siguientes credenciales:

- **Correo:** calificar@uvg.edu.gt
- **Contraseña:** secret123+

El dashboard aparecerá completamente construido sin ningún paso adicional.

---

## Dashboard

El dashboard está organizado en dos tabs:

**Tab 1 — Gestión de Inventario**
Monitoreo del estado del inventario por tienda y categoría, incluyendo productos en riesgo, valor inmovilizado y rotación de stock.

**Tab 2 — Proveedores y Abastecimiento**
Análisis del desempeño de proveedores, concentración de productos, tiempos de entrega y tasas de devolución.

---

## Notas técnicas

- PostgreSQL corre en el puerto `5434` del host
- Metabase corre en el puerto `3000` del host
- Todos los indicadores fueron construidos usando **Native query / SQL** en Metabase
