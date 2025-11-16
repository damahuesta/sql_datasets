# Catálogo de Datasets

Este repositorio contiene una colección de datasets para prácticas de SQL y análisis de datos. A continuación se detalla cada dataset con su estructura, campos y relaciones.

**Última actualización:** 2025-11-16

---

## Índice

**SQL_basics (9 tablas)**
1. [Car Inventory](#1-car-inventory)
2. [Star Wars](#2-star-wars)
3. [IMDB Titles](#3-imdb-titles)
4. [Spotify Tracks](#4-spotify-tracks)
5. [Top 50 Spotify](#5-top-50-spotify)
6. [Fortune 500](#6-fortune-500)
7. [Batman Movies](#7-batman-movies)
8. [ISDI Students](#8-isdi-students)
9. [ISDI Stock Prices](#9-isdi-stock-prices)

**dummies (8 tablas)**
10. [HR Departments (3 tablas)](#10-hr-departments)
11. [Supermarket (3 tablas)](#11-supermarket)
12. [University (2 tablas)](#12-university)

**company (7 tablas)**
13. [Company](#13-company)

---

## SQL_basics

### 1. Car Inventory

**Descripción**: Inventario de un concesionario de coches con información de vehículos en stock.

**Dataset**: \`SQL_basics\`  
**Tabla**: \`car_inventory\`

| Campo | Tipo | Descripción |
|-------|------|-------------|
| VehicleId | STRING | ID único del vehículo (matrícula) |
| Brand | STRING | Marca del vehículo |
| CarModel | STRING | Modelo del vehículo |
| Year | INTEGER | Año de fabricación |
| Color | STRING | Color |
| Transmission | STRING | Tipo de transmisión (Manual/Automática) |
| FuelType | STRING | Tipo de combustible (Gasolina/Híbrido/Diésel) |
| Mileage | FLOAT | Kilometraje |
| Price | FLOAT | Precio en euros |
| DateAdded | DATE | Fecha de ingreso al inventario |

**Registros**: ~100 vehículos

---

### 2. Star Wars

**Descripción**: Personajes del universo Star Wars con características físicas y origen.

**Dataset**: \`SQL_basics\`  
**Tabla**: \`starwars\`

| Campo | Tipo | Descripción |
|-------|------|-------------|
| name | STRING | Nombre del personaje |
| height | INTEGER | Altura en centímetros |
| mass | INTEGER | Masa en kilogramos |
| hair_color | STRING | Color de cabello |
| skin_color | STRING | Color de piel |
| eye_color | STRING | Color de ojos |
| birth_year | STRING | Año de nacimiento (BBY/ABY) |
| gender | STRING | Género |
| homeworld | STRING | Planeta de origen |
| species | STRING | Especie |

**Registros**: 87 personajes  
**Fuente**: SWAPI (Star Wars API)

---

### 3. IMDB Titles

**Descripción**: Top 1000 títulos de IMDB con las mejores puntuaciones.

**Dataset**: \`SQL_basics\`  
**Tabla**: \`imdb_titles\`

| Campo | Tipo | Descripción |
|-------|------|-------------|
| primaryTitle | STRING | Título de la película/serie |
| titleType | STRING | Tipo (movie, tvSeries, etc.) |
| startYear | INTEGER | Año de estreno |
| endYear | INTEGER | Año de finalización (series) |
| runtimeMinutes | INTEGER | Duración en minutos |
| genre | STRING | Géneros (separados por coma) |
| director | STRING | Director(es) |
| averageRating | FLOAT | Puntuación media (0-10) |
| numVotes | INTEGER | Número de votos |

**Registros**: ~1000 títulos  
**Fuente**: Datos públicos de IMDB

---

### 4. Spotify Tracks

**Descripción**: Dataset de canciones populares de Spotify con audio features.

**Dataset**: \`SQL_basics\`  
**Tabla**: \`spotify_tracks\`

| Campo | Tipo | Descripción |
|-------|------|-------------|
| Genre | STRING | Género musical |
| ArtistName | STRING | Nombre del artista |
| TrackName | STRING | Título de la canción |
| Popularity | INTEGER | Popularidad (0-100) |
| Duration | INTEGER | Duración en segundos |

**Registros**: ~5300 canciones  
**Fuente**: API pública de Spotify

---

### 5. Top 50 Spotify

**Descripción**: Top 50 canciones de Spotify por países específicos.

**Dataset**: \`SQL_basics\`  
**Tabla**: \`top50_spotify\`

| Campo | Tipo | Descripción |
|-------|------|-------------|
| Countries | STRING | Países donde fue top (códigos separados por coma) |
| TrackName | STRING | Título de la canción |
| ArtistName | STRING | Nombre del artista |
| AlbumName | STRING | Nombre del álbum |
| Popularity | INTEGER | Popularidad (0-100) |
| Date | DATE | Fecha del ranking |
| Duration | STRING | Duración (formato MM:SS) |

**Registros**: 50 canciones  
**Fuente**: API pública de Spotify

---

### 6. Fortune 500

**Descripción**: Listado de las 500 empresas más grandes de Estados Unidos con información financiera.

**Dataset**: \`SQL_basics\`  
**Tabla**: \`fortune\`

| Campo | Tipo | Descripción |
|-------|------|-------------|
| Rank | INTEGER | Posición en el ranking |
| Company | STRING | Nombre de la empresa |
| Sector | STRING | Sector de la empresa |
| Industry | STRING | Industria específica |
| Location | STRING | Ubicación (ciudad, estado) |
| Revenue | INTEGER | Ingresos (millones USD) |
| Profits | INTEGER | Beneficios (millones USD) |
| Employees | INTEGER | Número de empleados |

**Registros**: 500 empresas  
**Fuente**: Datos públicos de Fortune Magazine

---

### 7. Batman Movies

**Descripción**: Dataset con información de todas las películas de Batman, incluyendo actores, directores, recaudación y salarios.

**Dataset**: \`SQL_basics\`  
**Tabla**: \`batman_movies\`

| Campo | Tipo | Descripción |
|-------|------|-------------|
| Title | STRING | Título de la película |
| BatmanActor | STRING | Actor que interpreta a Batman |
| Director | STRING | Director de la película |
| ReleaseDate | DATE | Fecha de estreno |
| ReleaseYear | INTEGER | Año de estreno |
| BoxOfficeMillions | FLOAT | Recaudación en taquilla (millones USD) |
| BatmanSalaryMillions | FLOAT | Salario del actor de Batman (millones USD) |
| RuntimeMinutes | INTEGER | Duración en minutos |

**Registros**: ~15 películas

---

### 8. ISDI Students

**Descripción**: Base de datos de estudiantes de ISDI con información personal y académica.

**Dataset**: \`SQL_basics\`  
**Tabla**: \`isdi_students\`

| Campo | Tipo | Descripción |
|-------|------|-------------|
| IdEstudiante | INTEGER | ID único del estudiante |
| Nombre | STRING | Nombre |
| Apellido1 | STRING | Primer apellido |
| Apellido2 | STRING | Segundo apellido |
| FechaNacimiento | DATE | Fecha de nacimiento |
| Edad | INTEGER | Edad actual |
| Programa | STRING | Programa cursado |
| SiglasPrograma | STRING | Siglas del programa (DMBA, MDA, etc.) |
| Email | STRING | Email educativo |
| FechaMatriculacion | DATE | Fecha de matrícula |

**Registros**: ~100 estudiantes  
**Fuente**: Datos sintéticos

---

### 9. ISDI Stock Prices

**Descripción**: Precios históricos simulados de acciones de ISDI desde 2015.

**Dataset**: \`SQL_basics\`  
**Tabla**: \`isdi_stock_prices\`

| Campo | Tipo | Descripción |
|-------|------|-------------|
| Fecha | DATE | Fecha de la sesión |
| Apertura | FLOAT | Precio de apertura |
| Cierre | FLOAT | Precio de cierre |
| Maximo | FLOAT | Precio máximo del día |
| Minimo | FLOAT | Precio mínimo del día |
| Volumen | INTEGER | Volumen de transacciones |

**Registros**: ~1000 días de trading  
**Fuente**: Datos sintéticos

---

## dummies

### 10. HR Departments

**Descripción**: Tres tablas con la misma estructura para practicar operaciones UNION.

**Dataset**: \`dummies\`  
**Tablas**: 
- \`hhrr_dept_a_employees\`
- \`hhrr_dept_b_employees\`
- \`hhrr_dept_c_employees\`

| Campo | Tipo | Descripción |
|-------|------|-------------|
| EmployeeID | INTEGER | ID del empleado |
| Name | STRING | Nombre del empleado |
| Email | STRING | Email corporativo |

**Registros**: ~30 empleados por tabla  
**Nota**: Los empleados pueden estar duplicados entre departamentos para practicar UNION y UNION ALL.

---

### 11. Supermarket

**Descripción**: Dataset de supermercado con clientes, pedidos y precios de productos.

**Dataset**: \`dummies\`

#### 11.1. supermarket_customers

| Campo | Tipo | Descripción |
|-------|------|-------------|
| CustomerID | INTEGER | ID único del cliente |
| Name | STRING | Nombre del cliente |

**Registros**: ~100 clientes

#### 11.2. supermarket_orders

| Campo | Tipo | Descripción |
|-------|------|-------------|
| OrderID | INTEGER | ID único del pedido |
| CustomerID | INTEGER | FK a customers |
| Product | STRING | Producto pedido |
| OrderDate | DATE | Fecha del pedido |

**Registros**: ~500 pedidos

#### 11.3. supermarket_product_prices

| Campo | Tipo | Descripción |
|-------|------|-------------|
| ProductID | STRING | Nombre del producto |
| EffectiveDate | DATE | Fecha de vigencia del precio |
| Price | FLOAT | Precio en euros |

**Registros**: ~50 productos

---

### 12. University

**Descripción**: Dataset universitario con estudiantes y clases para practicar JOINs y valores NULL.

**Dataset**: \`dummies\`

#### 12.1. university_students

| Campo | Tipo | Descripción |
|-------|------|-------------|
| StudentID | INTEGER | ID único del estudiante |
| Name | STRING | Nombre del estudiante |
| ClassID | INTEGER | FK a classes (puede ser NULL) |

**Registros**: ~100 estudiantes

#### 12.2. university_classes

| Campo | Tipo | Descripción |
|-------|------|-------------|
| ClassID | INTEGER | ID único de la clase |
| ClassName | STRING | Nombre de la clase |

**Registros**: ~50 clases

---

## company

### 13. Company

**Descripción**: Dataset empresarial completo de una empresa ficticia con 150 empleados (personajes de series famosas). Incluye gestión de RRHH, estructura organizacional, historial de salarios, cambios de puesto y catálogo de servicios internos.

**Dataset**: \`company\`

#### 13.1. employees (Empleados)

| Campo | Tipo | Descripción |
|-------|------|-------------|
| employee_id | STRING | ID único del empleado (E0001, E0002...) |
| first_name | STRING | Nombre |
| last_name | STRING | Apellido |
| email | STRING | Email corporativo |
| phone | STRING | Teléfono |
| hire_date | DATE | Fecha de contratación |
| date_of_birth | DATE | Fecha de nacimiento |
| gender | STRING | Género (M/F) |
| is_active | STRING | Estado activo (Yes/No) |

**Registros**: 150 empleados

#### 13.2. departments (Departamentos)

| Campo | Tipo | Descripción |
|-------|------|-------------|
| department_id | STRING | ID único (D001, D002...) |
| department_name | STRING | Nombre del departamento |

**Departamentos disponibles**:
- D001: Dirección General
- D002: Tecnología
- D003: Recursos Humanos
- D004: Marketing
- D005: Ventas
- D006: Finanzas
- D007: Operaciones
- D008: Atención al Cliente

**Registros**: 8 departamentos

#### 13.3. current_salaries (Salarios Actuales)

| Campo | Tipo | Descripción |
|-------|------|-------------|
| employee_id | STRING | FK a employees |
| department_id | STRING | FK a departments |
| role | STRING | Rol actual del empleado |
| current_salary | FLOAT | Salario actual en euros |
| last_update | DATE | Fecha de última actualización |

**Roles disponibles**: Director, Gerente, Supervisor, Senior, Especialista, Analista, Asistente.

**Registros**: 150 registros

#### 13.4. job_history (Historial Laboral)

| Campo | Tipo | Descripción |
|-------|------|-------------|
| job_history_id | STRING | ID único (JH0001, JH0002...) |
| employee_id | STRING | FK a employees |
| department_id | STRING | FK a departments |
| role | STRING | Rol en ese periodo |
| start_date | DATE | Fecha de inicio |
| end_date | DATE | Fecha de fin (NULL si es actual) |

**Registros**: ~300 registros

#### 13.5. salary_history (Historial de Salarios)

| Campo | Tipo | Descripción |
|-------|------|-------------|
| salary_id | STRING | ID único (S0001, S0002...) |
| employee_id | STRING | FK a employees |
| job_history_id | STRING | FK a job_history |
| salary_amount | FLOAT | Monto del salario en euros |
| effective_date | DATE | Fecha efectiva del cambio |

**Registros**: ~400 registros

#### 13.6. service_catalog (Catálogo de Servicios)

| Campo | Tipo | Descripción |
|-------|------|-------------|
| service_code | STRING | Código único (S001, S002...) |
| service_name | STRING | Nombre del servicio |
| category | STRING | Categoría (Training, Health, Software, Coaching) |
| unit_price | FLOAT | Precio unitario en euros |
| active_from | DATE | Fecha de inicio de vigencia |
| active_to | DATE | Fecha de fin (NULL si activo) |

**Registros**: 20 servicios

#### 13.7. service_records (Registro de Servicios)

| Campo | Tipo | Descripción |
|-------|------|-------------|
| record_id | STRING | ID único del registro |
| employee_id | STRING | FK a employees |
| service_code | STRING | FK a service_catalog |
| service_date | DATE | Fecha del servicio |
| quantity | INTEGER | Cantidad de unidades |
| total_amount | FLOAT | Monto total (quantity × unit_price) |

**Registros**: ~800 registros

**Documentación detallada**: Ver [\`datasets/company/README.md\`](company/README.md) para más información sobre el dataset company.

---

## Notas Generales

- Los datasets están diseñados para prácticas educativas de SQL
- Algunos contienen datos sintéticos generados con scripts Python
- Fechas generalmente en formato ISO (YYYY-MM-DD)
- Algunos campos pueden contener valores NULL para simular datos reales
- Normalización: nombres de columnas en \`snake_case\` o \`PascalCase\` según el dataset

## Licencias y Fuentes

- **Company**: Datos sintéticos generados
- **IMDB**: Datos públicos de IMDB
- **Spotify**: API pública de Spotify
- **Fortune 500**: Datos públicos de Fortune Magazine
- **Star Wars**: SWAPI (Star Wars API)
- **ISDI Students/Stock Prices**: Datos sintéticos
- **Dummy datasets**: Datos sintéticos para prácticas
- **Batman**: Datos públicos recopilados

---

## Carga de Datos

Para cargar todos estos datasets en BigQuery, utiliza el script automatizado:

\`\`\`bash
cd scripts
./load_tables_to_bq.sh
\`\`\`

Este script cargará automáticamente:
- **SQL_basics**: 9 tablas
- **dummies**: 8 tablas  
- **company**: 7 tablas

**Total**: 24 tablas listas para usar en tus prácticas de SQL.
