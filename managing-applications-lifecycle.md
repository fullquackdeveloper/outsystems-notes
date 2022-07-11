# Managing the Applications Lifecycle

## Manage IT Users

* Roles assigned to a user for teams **override the default role** of the user.
* Roles assigned to a user on specific applications **override the default role** of the user and also **any role assigned through teams**.

## Permission levels for an environment

| Permision | Default Role | Team | Application |
| ----------- | ----------- | ----------- | ----------- |
| Full Control | User can manage **environment settings**. | NA | NA |
| Change and Deploy Applications | User can see **environment’s applications** in Service Studio, LifeTime and Service Center. User can change settings of **environment's applications**. | User can see **team’s applications** in Service Studio, LifeTime and Service Center. User can change settings of **team's applications**. | User can see **application** in Service Studio, LifeTime and Service Center. User can change settings of **application**. |
| Open and Debug Applications | User can open and debug **modules of environment's applications** using `Ctrl-O`. | User an open and debug **modules of team's applications** using `Ctrl-O`. | User can open and debug **modules of application** using `Ctrl-O`. |
| Monitor and Add Dependencies | User can add dependencies to the public elements of  **environment’s applications**. User can monitor  **environment’s applications** and **environment’s performance**. | User can add dependencies to the public elements of **team’s applications**. User can monitor **team’s applications**. | User can add dependencies to the public elements of **application**. User can monitor **application**. |
| List Applications | User can see **environment's applications** in LifeTime and Service Center. | User can see **teams's applications** in LifeTime and Service Center. | User can see **application** in LifeTime and Service Center. |
| Access | User can login to **environment**. | Same as **No Access**. | Same as **No Access**. |
| No Access | User cannot login to **environment**. | User cannot see **team’s applications** in LifeTime, Service Center or Service Studio. | User cannot see **application** in LifeTime, Service Center or Service Studio. |

## Specific permissions for an environment

| Permision | Default Role | Team | Application |
| ----------- | ----------- | ----------- | ----------- |
| Create Applications | User can create new applications in **environment** in Service Studio and Service Center. User can create new applications in **any team** in LifeTime. | User can create new applications in **team** in LifeTime. | NA |
| Add System Dependencies | User can add new dependencies to public elements of System module. | NA | NA |

## Infrastructure-wide permissions

| Permision | Default Role | Team | Application |
| ----------- | ----------- | ----------- | ----------- |
| Manage Users and Roles (Setting this ON also sets "Manage Teams and Application Roles" ON) | User can add/edit/remove IT users, roles and teams. User can turn on/off features in Technical Preview. | NA | NA |
| Manage Teams and Application Roles | User can add/remove IT users from **environment's team**. User can grant/revoke roles to IT users for **environment's applications**. User can edit **environment's teams** and access the audit logs. | User can add/remove IT users from **team**. User can grant/revoke roles to IT users for **team's applications**. User can edit **team** and access the **team's** audit logs. | User can grant/revoke roles to IT users for **application**. User can access  **application's** audit logs. |

## Allow Integrations With External Databases

- Create role with permission **Change and Deploy Applications**.
- Service Center > Administration > Database Connections.
- Grant **Publish** to role.
- To allow access to data on external database through extension, grant **Full Control**.