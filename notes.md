- como configurar cual es la app que se ejecuta por defecto en run start:dev
- como funciona el comando - nest generate app
- como funciona el comando - nest generate resource
- recordar despues de crear resources instalar @nestjs/microservices @grpc/grpc-js @grpc/proto-loader ts-proto
- Revisar muy bien que hace cada libraria que se instalo anteriormente.
- para que sirve el decorador MessagePattern de la libreria @nestjs/microservices
- Revisar la documentación para la ejecución de ts-proto: protoc --plugin=protoc-gen-ts_proto=.\node_modules\.bin\protoc-gen-ts_proto.cmd --ts_proto_out=. --ts_proto_opt=nestJs=true ./proto/auth.proto
- El comando anterior solo me sirvio ejecutandolo con npx.
- revisar cual es la funcionalidad del comando: nest generate lib common y por que se hicieron las modificaciones de carpetas
- revisar mas en detalle porque se debe mover el archivo auth.ts a la carpeta types de la libraria common
- Se realizan algunas modificaciones en cli coonfig de nestJs en el parametro de entry file, pero no entiendo para que.
- Interesante resaltar que la ruta del auth.proto en la configuración de gRPC, hace referencia a la carpeta como se genera em el dist
- En la archivo user.controller.ts, para que se utiliza en la creación de la clase 'implements'
- Como funciona la implementación del decorador @UsersServiceControllerMethods()
- En el archivo user.service.ts en la clase para que se utiliza 'implements onModuleInit'
- Revisar en detalle como funciona el servicio o la función queryUsers, en este paso revisar muy bien la aplicación de la libreria rxjs de node.js
- Revisar como crear el recurso users del apigetway directamente en la carpeta de apigetway.
- Revisar de forma detallada la forma como se configura el cliete gRPC desde el archivo users.module y validar porque no se hace desde app.module
- Revisar cuales son los parametros de la calse clientModule.register para la configuración del cliente gRPC.
- En el user.service.ts validar nuevamente como funciona el implements OnModuleInit (Ya tengo un poco mas de idea)
- Revisar en detalle como funciona la linea - private usersService: UsersServiceClient; - Y como se debe crear correctamente la interface en el archivo .proto para que funcione correctamente y porque.
- Revisar muy bien lo que hacen en el contructor de la clase -constructor(@Inject(AUTH_SERVICE) private client: ClientGrpc) {} -
- Revisar la documentación de nestJs relacionada con la implementación del cliente gRPC.

Video tutorial youtube: https://www.youtube.com/watch?v=UkWcjVWs2UQ&ab_channel=MichaelGuay
Repositorio: https://github.com/mguay22/nestjs-grpc/tree/8f2b1b300c6e1d2ef3c79d808000fff25a92ee11
