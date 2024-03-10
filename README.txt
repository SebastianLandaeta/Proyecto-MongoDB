Proyecto 2 de la materia Sistemas de Bases de Datos 2: Crear una base de datos con MongoDB Compass y Atlas, la cual tenga una colección "Curriculum"
y documentos dentro de ella, para que al momento de la presentación, se puedan realizar consultas a través del shell.

Integrantes: Sebastián Landaeta (28.240.979).
             Pablo Jiménez (30.110.259).
             María Martínez (24.412.465).

Link de Cluster: mongodb+srv://SebasLanda:10572820@cluster0.l2ydgpk.mongodb.net/

# Consultas para la demostración #
1) Actualizacion un campo de un documento específico.
db.getSiblingDB("Proy2-MongoBD").Curriculum.updateOne(
   { "_id": ObjectId("65be67c0d14335fa617496bc") },
   { $set: { "campo_a_actualizar": "nuevo_valor" } }
)

2) Hacer busquedas de interés.
db.getSiblingDB("Proy2-MongoBD").Curriculum.findOne({ "_id": ObjectId("65be67c0d14335fa617496bc") })

db.getSiblingDB("Proy2-MongoBD").Curriculum.find({
   $or: [
      { "resumen": "Un tipazo" },
      { "_id": ObjectId("65be67c0d14335fa617496bc") }
   ]
})

3) Eliminar un documento a partir del ID.
db.getSiblingDB("Proy2-MongoBD").Curriculum.deleteOne({ "_id": ObjectId("65be67c0d14335fa617496bc") })

4) Crear un nuevo documento.
db.getSiblingDB("Proy2-MongoBD").Curriculum.insertOne({
   "_id": ObjectId(), // Se generará automáticamente un nuevo ObjectId
   "Resumen": "Perfil profesional con experiencia en desarrollo de software.",
   "DatosPersonales": {
      "Nombre": "Ana García",
      "Dirección": "Av. Principal, Edif. Los Robles, Piso 5, Apt. 503",
      "Teléfono(s)": [
         "+58 412-1234567"
      ],
      "Email": "ana.garcia@example.com",
      "RedesSociales": {
         "LinkedIn": "linkedin.com/in/anagarcia",
         "Twitter": "@anagarcia_dev",
         "Instagram": "@anagarcia"
      }
   },
   "Educación": {
      "Básica": "U.E.C María Montessori.",
      "Media": "Colegio Los Pinos",
      "Universitaria": "Universidad Central de Venezuela, Ingeniería en Sistemas",
      "Otros": [
         "Curso de Desarrollo de Aplicaciones Móviles",
         "Certificación en Gestión de Proyectos (PMP)"
      ]
   },
   "Laboral": {
      "Pasantía": {
         "Empresa": "Google",
         "Cargo": "Desarrollador de Software",
         "Período": "Febrero 2023 - Abril 2023"
      },
      "Trabajos": [
         {
            "Tipo": "Contratado",
            "Empresa": "Microsoft",
            "Cargo": "Ingeniero de Software",
            "Período": "Mayo 2023 - Presente"
         }
      ]
   },
   "ConocimientosTécnicos": {
      "OS": [
         "Windows",
         "Linux",
         "macOS"
      ],
      "LenguajeDesarrollo": [
         "JavaScript",
         "Java",
         "Python",
         "Swift"
      ],
      "BasesDeDatos": [
         "MongoDB",
         "MySQL",
         "PostgreSQL"
      ],
      "OtrosSoftwares": [
         "Git",
         "Visual Studio Code",
         "Adobe Photoshop"
      ]
   },
   "InteresesPersonales": [
      "Fotografía",
      "Senderismo",
      "Cocina",
      "Música"
   ]
})
