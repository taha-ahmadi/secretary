## Routes
+ resource::achievements
+ resource::successes
+ resource::awards
+ resource::appointments
+ resource::connections
+ resource::goals
+ resource::projects

## Databases and structures
> all fields is nullable
+ users: user_id(Int), name(Varchar), email(Varchar), password(Varchar)
+ achievements: title(Varchar), description(Varchar), category(Varchar), user_id(Int): K to users
+ successes: title(Varchar), description(Varchar), category(Varchar), user_id(Int): K to users
+ awards:   award(Varchar), title(Varchar), for(Varchar), user_id(Int): K to users
> award: What did I reward myself with?
> for: achievement/success
+ appointments: title(Varchar), description(Varchar), who(Varchar), date-time(Date-time), user_id(Int): K to users
> who: @mention the people I meet.
+ connections: name(Varchar), contact(Varchar), for(Varchar), description(Varchar), user_id(Int): K to users
> contact: email/phone_number/address or ...
> for: What can I contact for?
+ goals: title(Varchar), description(Varchar), time(Varchar), user_id(Int): K to users
> time: for long time or short time.
+ project_management: project_id(Int), title(Varchar), description(Varchar)
+ project_todos: title(Varchar), description(Varchar), project_id(Int): K to project_management

## Controllers
Controller: ProjectTodo
Controller: User
Controller: Project
Controller: Goals
Controller: Connections
Controller: Appointments
Controller: Awards
Controller: Successes
Controller: Achievements
Controller: Home

## Todos


## Features
**Mention**: @mention people in the connections table in title and description field for all tabs.

