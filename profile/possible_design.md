# Disennio posible de entidades y estructuras

El objetivo de este documento es alinear las diferentes entidades comunes que usa todo el equipo


## Diagramas de Clases

Diagrama de clases principales que sirven para la resolucion de los algoritmos
```plantuml
@startuml
abstract class Solver {
~ groups: List<Group>
~ tutors: List<Tutor>
+ solve(): AssigmentResult 
}


class DeliveryFlowSolver extends Solver {
- evaluators: evaluators
- possible_dates: List<DeliveryDate>

- create_source_edges(List nodes, int base_capacity )
- create_sink_edges(List nodes, int base_capacity)
- create_groups_graph(): DiGraph
- create_evaluator_graph(): DiGraph
- max_flow_min_cost(DiGraph graph): Dict
+ solve(): AssigmentResult 
}

class TopicTutorFlowSolver extends Solver {
+ solve(): AssigmentResult 
}

class DeliveryLPSolver extends Solver {
+ solve(): AssigmentResult 
}

abstract class Group {
- id: int
- tutor: Tutor
}

abstract class Tutor{
- id: int
- groups: List<Group>
}

class FinalStateGroup extends Group{
- avaliable_dates: List<DeliveryDate>
- remove_dates(List<DeliveryDate> dates): void
- is_tutored_by(Tutor tutor): bool
+ avaliable_dates(): List<DeliveryDate>
+ id(): int
}

class InitialStateGroup extends Group{
- topics: List<Topic>
+ assign_tutor(Tutor tutor):void
+ id(): int
}

class FinalStateTutor extends Tutor{
- avaliable_dates: List<DeliveryDate>
+ avaliable_dates(): List<DeliveryDate>
+ id(): int
}

class InitialStateTutor extends Tutor{
- topics: List<Topic>
- group_capacity: int
+ assign_group(Group group):void
+ id(): int
}

class DeliveryDate{
- week: int
- day: int
- hour: int

+ label(): String
}

class Topic{
- id: int
- priority: int
- title: String
}

@enduml
```
## Estructura del proyecto
