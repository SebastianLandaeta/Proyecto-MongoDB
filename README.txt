Proyecto 2 de la materia Sistemas de Bases de Datos 2.

Integrantes: Sebastián Landaeta (28.240.979).
             Pablo Jiménez ().
             María Martínez (24.412.465)

Link de Cluster: mongodb+srv://SebasLanda:10572820@cluster0.l2ydgpk.mongodb.net/
<<<<<<< Updated upstream
=======


actualizacion de Datos
db.getSiblingDB("Proy2-MongoBD").Curriculum.updateOne(
   { "_id": ObjectId("65be67c0d14335fa617496bc") },
   { $set: { "campo_a_actualizar": "nuevo_valor" } }
)

hacer busquedas de interes 
db.getSiblingDB("Proy2-MongoBD").Curriculum.findOne({ "_id": ObjectId("65be67c0d14335fa617496bc") })

eliminar un documento a partir del ID 
db.getSiblingDB("Proy2-MongoBD").Curriculum.deleteOne({ "_id": ObjectId("65be67c0d14335fa617496bc") })


estas querys se usan en la shell de Mongodb Compass y todas funcionan de acuerdo a las necesidades de la busqueda 

>>>>>>> Stashed changes
