# lab10multiplataforma

    import 'package:flutter/material.dart';
    
    void main() {
      runApp(MyApp());
    }
    
    class MyApp extends StatelessWidget {
      const MyApp({Key? key}) : super(key: key);
    
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: const Text('Clasicos del Madrid'),
            ),
            body: SingleChildScrollView(
              child: Column(
                children: const [
                  EventCard(
                    eventName: 'Real Madrid vs Barcelona',
                    eventImage: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSYPAcSlaka-nnrGWeY2PC9aMaAPRgrfhY1cA&usqp=CAU',
                    eventInfo: 'Fecha: 21 de Abril 2024',
                  ),
                  EventCard(
                    eventName: 'Real Madrid vs Barcelona',
                    eventImage: 'https://www.fcbarcelonanoticias.com/uploads/s1/13/94/01/8/cronica-del-fc-barcelona-supercopa-1.jpeg',
                    eventInfo: 'Fecha: 14 de Enero 2024',
                  ),
                  EventCard(
                    eventName: 'Real Madrid vs Barcelona',
                    eventImage: 'https://a.espncdn.com/media/motion/2023/1028/Hu_231028_RESUMEN_CLASICO_COM_REV1/Hu_231028_RESUMEN_CLASICO_COM_REV1.jpg',
                    eventInfo: 'Fecha: 28 de Octubre 2023',
                  ),
                  EventCard(
                    eventName: 'Real Madrid vs Barcelona',
                    eventImage: 'https://d16f573ilcot6q.cloudfront.net/wp-content/uploads/2023/04/Untitleddfgggg.jpg',
                    eventInfo: 'Fecha: 5 de Abril 2023',
                  ),
                ],
              ),
            ),
          ),
        );
      }
    }
    
    class EventCard extends StatelessWidget {
      final String eventName;
      final String eventImage;
      final String eventInfo;
    
      const EventCard({
        required this.eventName,
        required this.eventImage,
        required this.eventInfo,
        Key? key,
      }) : super(key: key);
    
      @override
      Widget build(BuildContext context) {
        return Card(
          child: Column(
            children: <Widget>[
              Image.network(
                eventImage,
                fit: BoxFit.cover,
                width: double.infinity,
                height: 200,
              ),
              Padding(
                padding: const EdgeInsets.all(8.0),
                child: Column(
                  crossAxisAlignment: CrossAxisAlignment.start,
                  children: <Widget>[
                    Text(
                      eventName,
                      style: const TextStyle(
                        fontSize: 20,
                        fontWeight: FontWeight.bold,
                      ),
                    ),
                    const SizedBox(height: 10),
                    Text(
                      eventInfo,
                      style: const TextStyle(
                        fontSize: 16,
                      ),
                    ),
                  ],
                ),
              ),
            ],
          ),
        );
      }
    }

----------------------------------------------------
LAB10
