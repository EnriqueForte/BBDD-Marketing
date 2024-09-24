# BBDD-Marketing
Proyecto de IBM SkillBuild con SQL Server

Proyecto de Base de Datos de Marketing
Este proyecto consiste en crear una base de datos con 13 tablas relacionadas, las cuales combinaremos y consultaremos a través del lenguaje Transact SQL.

II. Creación de las Tablas
A continuación, se detallan las 13 tablas que debes crear, junto con sus campos y especificaciones:

1. Tabla Clientes
Contiene los datos de los clientes.

IdCliente: int, no admite nulos, IDENTITY, PRIMARY KEY
Nombre: varchar(50), no admite nulos
Apellido: varchar(50), no admite nulos
Fnacimiento: date, no admite nulos
Domicilio: varchar(50), no admite nulos
idPais: char(3), no admite nulos
Telefono: varchar(12), admite nulos
Email: varchar(30), no admite nulos
Observaciones: varchar(1000), admite nulos
FechaAlta: datetime, no admite nulos
2. Tabla Record
Tabla de hechos que contiene el historial de campañas.

IdRecord: int, no admite nulos, IDENTITY, PRIMARY KEY
FechaRecord: date, no admite nulos
Observaciones: varchar(1000), admite nulos
3. Tabla RecordCliente
Contiene el historial de campañas por las que ha pasado el cliente. Esta tabla tiene una PRIMARY KEY compuesta por los tres campos.

idRecord: int, no admite nulos
IdCliente: int, no admite nulos
IdCampania: int, no admite nulos
Nota: Cuando veas una instrucción como esta, recuerda que el nombre que debes usar en tu tabla es el que está entre paréntesis.

4. Tabla Pais
Contiene los países de origen de los clientes.

IdPais: char(3), no admite nulos, PRIMARY KEY
NombrePais: varchar(100), no admite nulos
5. Tabla HoraCaptacion
Contiene la hora en la cual los clientes se registraron en las campañas.

idHCaptacion: int, no admite nulos, IDENTITY, PRIMARY KEY
FechaCaptacion: date, no admite nulos
EstadoCaptacion: smallint, no admite nulos
Observaciones: varchar(1000), admite nulos
6. Tabla HoraCapClienteCampania
Contiene la hora en la cual se registraron en las campañas los clientes. Esta tabla tiene una PRIMARY KEY compuesta por los tres campos.

idHCaptacion: int, no admite nulos, PRIMARY KEY
idCliente: int, no admite nulos, PRIMARY KEY
idCampania: int, no admite nulos, PRIMARY KEY
7. Tabla HorarioEstado
Contiene la dimensión del horario con la descripción de un estado.

IdEstado: smallint, no admite nulos, IDENTITY, PRIMARY KEY
Descripcion: varchar(50), no admite nulos
8. Tabla Producto
Contiene los productos asociados a las campañas.

IdProducto: int, no admite nulos, IDENTITY, PRIMARY KEY
Producto: varchar(100), no admite nulos
9. Tabla Compra
Contiene las compras en dinero que han realizado los clientes.

IdCompras: int, no admite nulos, IDENTITY, PRIMARY KEY
Concepto: int, no admite nulos
Fecha: datetime, no admite nulos
Monto: money, no admite nulos
Observaciones: varchar(1000), admite nulos
10. Tabla CompraCliente
Conecta las compras con los clientes y su captación. La PRIMARY KEY de esta tabla está compuesta por los tres campos.

IdCompras: int, no admite nulos
IdCliente: int, no admite nulos
idHCaptacion: int, no admite nulos
11. Tabla Campania
Contiene la dimensión de campañas que han realizado los clientes.

IdCampania: int, no admite nulos, IDENTITY, PRIMARY KEY
NombreCampaña: varchar(50), no admite nulos
12. Tabla CampaniaProducto
Contiene las relaciones entre las campañas y los productos.

IdCampania: int, no admite nulos, PRIMARY KEY
IdProducto: int, no admite nulos, PRIMARY KEY
Descripcion: varchar(100), no admite nulos
13. Tabla ConceptoCompra
Contiene la dimensión de conceptos de compra.

IdConcepto: int, no admite nulos, IDENTITY, PRIMARY KEY
Concepto: varchar(100), no admite nulos

