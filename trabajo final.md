# trabajo-
@@ -1,34 +1,34 @@
usando el  sistema ;
utilizando  System . Colecciones . Genérico ;
utilizando  System . Enhebrado ;
utilizando  System . Enhebrado . Tareas ;
usando  Dominio ;
usando  MediatR ;
utilizando  Microsoft . EntityFrameworkCore ;
usando  persistencia ;
 Aplicación de espacio de nombres . Ocupaciones
{
    público  de clase  ListById {
        público  de clase  IDConsulta : IRequest < Actividad > {
            public  Guid  _guid ;
            
            public  QueryId ( Guid  guid ) {
                _guid  =  guid ;
                
            }
           
        }
    
    público  de clase  Handler : IRequestHandler < IDConsulta , Actividad >
        {
             privado de  solo lectura  DataContext  _context ;
             Manejador público ( contexto DataContext  ) {
                _context  =  contexto ;
            }
              pública  asíncrono  de tareas < Actividad > Mango ( IDConsulta  solicitud , CancellationToken  CancellationToken ) {
            pública  asíncrono  de tareas < Actividad > Mango ( IDConsulta  solicitud , CancellationToken  CancellationToken ) {
                volver  aguardar  _context . Actividades . FindAsync ( solicitud . _Guid );
            }

    }
    }
       
}
