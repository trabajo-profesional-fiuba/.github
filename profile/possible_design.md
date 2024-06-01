# Diseño posible de entidades y estructuras

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


abstract class DeliverySolver extends Solver{
~ available_dates: List<DeliveryDate>
+ solve(): AssigmentResult
}

abstract class GroupTutorSolver extends Solver{
~ topics: List<DeliveryDate>
+ solve(): AssigmentResult
}

interface Formatter {}

Solver o-up-Formatter

class DeliveryFlowSolver extends DeliverySolver{
- evaluators: evaluators
- possible_dates: List<DeliveryDate>

- create_source_edges(List nodes, int base_capacity )
- create_sink_edges(List nodes, int base_capacity)
- create_groups_graph(): DiGraph
- create_evaluator_graph(): DiGraph
- max_flow_min_cost(DiGraph graph): Dict
+ solve(): AssigmentResult 
}

class TopicTutorFlowSolver extends GroupTutorSolver {
+ solve(): AssigmentResult 
}

class DeliveryLPSolver extends DeliverySolver{
+ solve(): AssigmentResult 
}

class Group {
- id: int
- tutor: Tutor
+ assign(item, Group group):void
- assign_tutor(Tutor tutor)
- assign_date(DeliveryDate dd)
+ preference_of(int item_id )
}

class Tutor{
- id: int
- groups: List<Group>
- name: String
- email: String
+ assign_group(Group group):void
}

interface TutorState{}
interface GroupState{}

Group *-right- GroupState

class FinalStateGroup implements GroupState {
- avaliable_dates: List<DeliveryDate>
- assigned_date: DeliveryDate
- remove_dates(List<DeliveryDate> dates): void
- is_tutored_by(Tutor tutor): bool
- assign_date(DeliveryDate dd)
+ avaliable_dates(): List<DeliveryDate>
+ assign(item, Group group):void

}

class InitialStateGroup implements GroupState{
- topics: List<Topic>
+ assign(item, Group group):void
- assign_tutor(Tutor tutor)
}

class FinalStateTutor implements TutorState{
- avaliable_dates: List<DeliveryDate>
- assigned_dates: List<DeliveryDate>
+ avaliable_dates(): List<DeliveryDate>
+ id(): int
}

class InitialStateTutor implements TutorState{
- topics: List<Topic>
- global_capacity: int

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
- cost: int
- capacity: int
- title: String
}

class AssigmentResult{
- id: int
- groups: List<Group>
- tutors: List<Tutor>
- evaluators: List<Evaluators>

+ delivery_date(int group_id): DeliveryDate
+ delivery_date_evaluator(int evaluator_id)
}



Tutor *-right- TutorState

@enduml
```
![image](https://github.com/trabajo-profesional-fiuba/.github/assets/56161645/c2c17a25-bb0e-42ee-8d16-e6a4a919d0e0)

## Estructura del proyecto

```
assignment-service/
├── pyproject.toml
├── poetry.lock
├── README.md
├── .gitignore
├── 
├── src/
│   └── algorithms/
│       ├── __init__.py
│       └── ...
│   └── model/
│       ├── group/
│       ├── tutor/
│       └── utils/
│         ├── delivery_date/
│         ├── evaluator.py
│         ├── topic.py
│── tests/
│   ├── __init__.py
│   └── ...
    
```
## Possible Folder Structure

![AssignmentService](https://github.com/trabajo-profesional-fiuba/.github/assets/75905945/f109eabb-8e45-456e-b08f-02c64df8d427)
